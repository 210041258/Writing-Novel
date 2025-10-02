
Sub-Cars Deatils to complete study: https://plexe.car2x.org/tutorial/example2/ to /example5/ 



Car.ned is the deatils about the operation of the car which will be directed to the car
---------------------------

example code of car.ned

--------

enum ACTIVE_CONTROLLER {DRIVER = 0, ACC = 1, CACC = 2, FAKED_CACC = 3, PLOEG = 4, CONSENSUS = 5, FLATBED = 6, MYCC = 7}; // 87 = 86.7

--------

#define CC_PAR_MYCC_KD "ccmykd"  //k_d constant for new controller
#define CC_PAR_MYCC_KS "ccmyks"  //alhamdullah

--------

double myccKd = default(0.6); // 1 for kd
double myccKs = default(1); // 0.6 for ks

--------

*.node[*].scenario.myccKd = 0.2 // 0.4 for kd future usage
*.node[*].scenario.myccKs = 0.4 // 0.2 for ks future demonstration


--------
 // main controllr 
cntr = c(
                  // ac : kd2ks-cntr * scenario * default
   "ACC (0.3 s)", // acc : 0.3 * 0.4 * 1
   "ACC (1.2 s)", // acc : 1.2 * 0.2 * 0.6
   "CACC",
   "PLOEG",
   "CONSENSUS",
   "FLATBED",
   "MYCC"
)


---------------------------

CARS NAMES :  

Alfa Romeo 147 1.6 TS [(GZ-JXX-2) & (01-10) & (11)] -> {The Alfa Romeo reaches about 190 km/h} -> {in-bd-l (1)}: 
  https://upload.wikimedia.org/wikipedia/commons/c/c0/2002_Alfa_Romeo_147_(MY02)_Selespeed_Twin_Spark_5-door_hatchback_(2010-11-28).jpg

good car:
  , and a Alfa Romeo 147 1.6 TS [(LxxL)] -> {the Bugatti reaches the stunning speed of 200 km/h.} -> {in-bd-l (2)}:
  https://upload.wikimedia.org/wikipedia/commons/c/c9/Bugatti_Veyron_16.4_%E2%80%93_Frontansicht_(1),_5._April_2012,_D%C3%BCsseldorf.jpg


wastage car :
  , an Audi R8 (WJG-YX,AFG-YX) -> {the Audi roughly 300 km/h} -> {out-bd (1) , in-bd (1)} :
  https://upload.wikimedia.org/wikipedia/commons/3/3b/2013_red_Audi_R8_V10_coupe_in_Spain_(11089737186).jpg
  
  , and a Bugatti Veyron (W-XJDX-YX) -> {the Bugatti reaches the stunning speed of 400 km/h.} -> {out-bd (3) , in-bd (1)}:
  https://upload.wikimedia.org/wikipedia/commons/c/c9/Bugatti_Veyron_16.4_%E2%80%93_Frontansicht_(1),_5._April_2012,_D%C3%BCsseldorf.jpg
