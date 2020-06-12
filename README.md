# Sl_lab_2_183193
Група на код: 6
Control Flow Graph 

public List<Integer> function(List<Angle> angleList) {
        List<Integer> result = new ArrayList<>();	//A

        for (int i = 0; i < angleList.size(); i++) {	//B
            int deg = angleList.get(i).getDegrees();	//C
            int min = angleList.get(i).getMinutes();	//C
            int sec = angleList.get(i).getSeconds();	//C
            if (deg >= 0 && deg < 360) {				//D
                if (min < 0 || min > 59)				 //L
                    throw new RuntimeException("The minutes of the angle are not valid!");//X
                else {						//  i
                    if (sec < 0 || sec > 59)	//j
                        throw new RuntimeException("The seconds of the angle are not valid");//Y
                    else	//	K
                        result.add(deg * 3600 + min * 60 + sec);	//Z
                }
            } else if (deg == 360) {		// E
                if (min == 0 && sec == 0)	//H
                    result.add(deg * 3600 + min * 60 + sec);		//Q
                else	//E-b
                    throw new RuntimeException("The angle is greater then the maximum");	//W
            } else {	//	F
                throw new RuntimeException("The angle is smaller or greater then the minimum"); //P
            }
        }
        return result;	// V

    }

![graf](https://user-images.githubusercontent.com/63548247/84515959-70440300-accd-11ea-83f3-2d9a2d9e1b70.jpg)
