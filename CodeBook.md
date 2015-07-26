### Code Book for the Tidy Data Assignment

The tidy data frame in "finaldataset.txt" has 68 variables, described below with their unit. The explanation of the procedure followed to obtain the original measurements can be found with the original data in the "README.txt" and the "features\_info.txt" files. The description of the steps applied to obtain the final tidy data set can be found on the README.md file in this repository.  

***

**Notes on the units:**
*	The units are written in their stantardardized form, eg rad.s<sup>-1</sup> for radians/second
*	The variables representing a signal which has been derived in time see their units divided by the time unit (seconds): for example,  a velocity in rad.s<sup>-1</sup> is derived into an acceleration in rad.s<sup>-2</sup>
*	The "magnitude" variables are obtained after a normalization (Euclidean norm), they are unit-less
*	The Fast Fourier Transform is a discrete fourier transform; it does not change the unit of the signals

***
**activity**

Description of the activity performed when the measurements were taken.  
6 levels:   
1 WALKING  
2 WALKING_UPSTAIRS  
3 WALKING_DOWNSTAIRS  
4 SITTING  
5 STANDING  
6 LAYING    
  
***    
**subject**  

Numbers corresponding to the identifiers of the volunteers taking part in the experiment.   
Ranges from 1 to 30  

****
**IMPORTANT NOTE: the following variables are *average values* of the corresponding variables in the original dataset, computed for each activity and each subject.**  


***
**tbodyacc.mean...x**  

Mean of the body linear acceleration signal along the X axis  
unit: g (standard gravity unit)  

***
**tbodyacc.mean...y**  

Mean of the body linear acceleration signal along the Y axis  
unit: g (standard gravity unit)  

***
**tbodyacc.mean...z**  

Mean of the body linear acceleration signal along the Z axis  
unit: g (standard gravity unit)  

***
**tbodyacc.std...x** 

Standard deviation of the body linear acceleration signal along the X axis  
unit: g (standard gravity unit)  

***
**tbodyacc.std...y**  

Standard deviation of the body linear acceleration signal along the Y axis  
unit: g (standard gravity unit)  

***
**tbodyacc.std...z**  

Standard deviation of the body linear acceleration signal along the Z axis  
unit: g (standard gravity unit)  

***
**tgravityacc.mean...x** 

Mean of the gravity acceleration signal along the X axis  
unit: g (standard gravity unit) 
			
***
**tgravityacc.mean...y**  

Mean of the gravity acceleration signal along the Y axis  
unit: g (standard gravity unit) 
			
***
**tgravityacc.mean...z**  

Mean of the gravity acceleration signal along the Z axis  
unit: g (standard gravity unit) 
			
***
**tgravityacc.std...x**  

Standard deviation of the gravity acceleration signal along the X axis  
unit: g (standard gravity unit) 
			
***
**tgravityacc.std...y**  

Standard deviation of the gravity acceleration signal along the Y axis  
unit: g (standard gravity unit) 
			
***
**tgravityacc.std...z** 

Standard deviation of the gravity acceleration signal along the Z axis  
unit: g (standard gravity unit) 
			
***
**tbodyaccjerk.mean...x**  

Mean of the body linear acceleration along the X axis, derived in time   
unit: g.s<sup>-1</sup> 
			
***
**tbodyaccjerk.mean...y**  

Mean of the body linear acceleration along the Y axis, derived in time   
unit: g.s<sup>-1</sup> 
			
***
**tbodyaccjerk.mean...z** 

Mean of the body linear acceleration along the Z axis, derived in time  
unit: g.s<sup>-1</sup> 
			
***
**tbodyaccjerk.std...x**  

Standard deviation of the body linear acceleration along the X axis, derived in time  
unit: g.s<sup>-1</sup> 
			
***
**tbodyaccjerk.std...y**  

Standard deviation of the body linear acceleration along the Y axis, derived in time  
unit: g.s<sup>-1</sup> 
			
***
**tbodyaccjerk.std...z**  

Standard deviation of the body linear acceleration along the Z axis, derived in time  
unit: g.s<sup>-1</sup> 
			
***
**tbodygyro.mean...x**  

Mean of the body angular velocity along the X axis  
unit: rad.s<sup>-1</sup> 
	
***
**tbodygyro.mean...y**  

Mean of the body angular velocity along the Y axis  
unit: rad.s<sup>-1</sup> 
			
***
**tbodygyro.mean...z**  

Mean of the body angular velocity along the Z axis   
unit: rad.s<sup>-1</sup> 
			
***
**tbodygyro.std...x**    

Standard deviation of the body angular velocity along the X axis  
unit: rad.s<sup>-1</sup> 
			
***
**tbodygyro.std...y**    

Standard deviation of the body angular velocity along the Y axis  
unit: rad.s<sup>-1</sup> 
	
***
**tbodygyro.std...z**    

Standard deviation of the body angular velocity along the Z axis  
unit: rad.s<sup>-1</sup> 
	
***
**tbodygyrojerk.mean...x**    

Mean of the body angular velocity along the X axis, derived in time (acceleration)  
unit: rad.s<sup>-2</sup> 
			
***
**tbodygyrojerk.mean...y**    

Mean of the body angular velocity along the Y axis, derived in time (acceleration)  
unit: rad.s<sup>-2</sup> 
	
***
**tbodygyrojerk.mean...z**    

Mean of the body angular velocity along the Z axis, derived in time (acceleration)  
unit: rad.s<sup>-2</sup> 
	
***
**tbodygyrojerk.std...x**    

Standard deviation of the body angular velocity along the X axis, derived in time 			(acceleration)  
unit: rad.s<sup>-2</sup> 
	
***
**tbodygyrojerk.std...y**    
Standard deviation of the body angular velocity along the Y axis, derived in time 			(acceleration)  
unit: rad.s<sup>-2</sup> 
	
***
**tbodygyrojerk.std...z**    
Standard deviation of the body angular velocity along the Z axis, derived in time 			(acceleration)  
unit: rad.s<sup>-2</sup> 
	
***
**tbodyaccmag.mean..**    

Mean of the magnitude of the body linear acceleration    

***
**tbodyaccmag.std..**    

Standard deviation of the magnitude of the body linear acceleration  

***
**tgravityaccmag.mean..**    

Mean of the magnitude of the gravity acceleration    

***
**tgravityaccmag.std..**    

Standard deviation of the magnitude of the gravity acceleration    

***
**tbodyaccjerkmag.mean..**    

Mean of the magnitude of the body linear acceleration derived in time      

***
**tbodyaccjerkmag.std..**    

Standard deviation of the magnitude of the body linear acceleration derived in time      

***
**tbodygyromag.mean..**    

Mean of the magnitude of the body angular velocity  

***
**tbodygyromag.std..**    

Standard deviation of the magnitude of the body angular velocity  

***
**tbodygyrojerkmag.mean..**    

Mean of the magnitude of the body angular acceleration 

***
**tbodygyrojerkmag.std..**    

Standard deviation of the magnitude of the body angular acceleration 

***
**fbodyacc.mean...x**    

Mean of the body linear acceleration signal along the X axis, after a Fast Fourier Transform    
unit: g

***
**fbodyacc.mean...y**    

Mean of the body linear acceleration signal along the Y axis, after a Fast Fourier Transform    
unit: g

***
**fbodyacc.mean...z**    

Mean of the body linear acceleration signal along the Z axis, after a Fast Fourier Transform    
unit: g

***
**fbodyacc.std...x**    

Standard deviation of the body linear acceleration signal along the X axis, after a Fast Fourier Transform    
unit: g

***
**fbodyacc.std...y**    

Standard deviation of the body linear acceleration signal along the Y axis, after a Fast Fourier Transform    
unit: g

***
**fbodyacc.std...z**    

Standard deviation of the body linear acceleration signal along the Z axis, after a Fast Fourier Transform    
unit: g

***
**fbodyaccjerk.mean...x**    

Mean of the body linear acceleration along the X axis, derived in time, after a Fast Fourier Transform      
unit: g.s<sup>-1</sup> 

***
**fbodyaccjerk.mean...y**    

Mean of the body linear acceleration along the Y axis, derived in time, after a Fast Fourier Transform     
unit: g.s<sup>-1</sup> 

***
**fbodyaccjerk.mean...z**    

Mean of the body linear acceleration along the Z axis, derived in time, after a Fast Fourier Transform     
unit: g.s<sup>-1</sup> 

***
**fbodyaccjerk.std...x**    

Standard deviation of the body linear acceleration along the X axis, derived in time, after a Fast Fourier Transform  unit: g.s<sup>-1</sup> 

***
**fbodyaccjerk.std...y**    

Standard deviation of the body linear acceleration along the Y axis, derived in time, after a Fast Fourier Transform  unit: g.s<sup>-1</sup> 

***
**fbodyaccjerk.std...z** 

Standard deviation of the body linear acceleration along the Z axis, derived in time, after a Fast Fourier Transform  unit: g.s<sup>-1</sup> 

***
**fbodygyro.mean...x**    

Mean of the body angular velocity along the X axis, after a Fast Fourier Transform      
unit: rad.s<sup>-1</sup> 

***
**fbodygyro.mean...y**    

Mean of the body angular velocity along the Y axis, after a Fast Fourier Transform      
unit: rad.s<sup>-1</sup> 

***
**fbodygyro.mean...z** 

Mean of the body angular velocity along the Z axis, after a Fast Fourier Transform        
unit: rad.s<sup>-1</sup> 

***
**fbodygyro.std...x**    

Standard deviation of the body angular velocity along the X axis, after a Fast Fourier Transform          
unit: rad.s<sup>-1</sup> 

***
**fbodygyro.std...y**    

Standard deviation of the body angular velocity along the Y axis, after a Fast Fourier Transform          
unit: rad.s<sup>-1</sup> 

***
**fbodygyro.std...z** 

Standard deviation of the body angular velocity along the Z axis, after a Fast Fourier Transform          
unit: rad.s<sup>-1</sup> 

***
**fbodyaccmag.mean..**    

Mean of the magnitude of the body linear acceleration, after a Fast Fourier Transform     
   
***
**fbodyaccmag.std..**    

Standard deviation of the magnitude of the body linear acceleration, after a Fast Fourier Transform     

***
**fbodyaccjerkmag.mean..** 

Mean of the magnitude of the body linear acceleration derived in time, after a Fast Fourier Transform          

***
**fbodyaccjerkmag.std..**    

Standard deviation of the magnitude of the body linear acceleration derived in time, after a Fast Fourier Transform  

***
**fbodygyromag.mean..**    

Mean of the magnitude of the body angular velocity, after a Fast Fourier Transform     

***
**fbodygyromag.std..** 

Standard deviation of the magnitude of the body angular velocity, after a Fast Fourier Transform     
 
***
**fbodygyrojerkmag.mean..**    

Mean of the magnitude of the body angular acceleration, after a Fast Fourier Transform     

***
**fbodygyrojerkmag.std..**    

Standard deviation of the magnitude of the body angular acceleration, after a Fast Fourier Transform     

***
