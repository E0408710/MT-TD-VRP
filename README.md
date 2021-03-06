# MT-TD-VRP
The real world data from Singapore Coca-Cola.

File 1: Customer2ID.txt
  The number of customers in data files are serial numbers generated by Coca-Cola. eg. 502785770.
  This file will map such serial numbers to the Virtual Number from 1 to 1987.
  
File 2: ODMatrix.txt
  This file is a distance matrix file. 
  Each row contains three number (a,b,c), where a and b are customers' Virtual Number and 
  c is the distance in real-life between a and b.
  
## Files in "cola":
    These files are the data using in this work.
   
    First line: Customer number need to be served.
    Second line: Capacity of the Vehicle.
    Third line: Maximum distance limit of each trip.
    
    [node]
    depot
    
    [pickup]
    idx; serial number; load; service_time
    
    
    [Speed 0]
    [Speed 1]
    [Speed 2]
    [Speed 3]
    [Speed 4]
    Five time zone with different speed profile: 
    eg. " 0.0 120.0 0.0 0.5" : means from time 0 to time 120, the speed is set to 0.5

    [speed choose matrix]
    For each arc, it has a speed profile.
    eg.  the link (0,4) is assigned with speed profile 1, which is given by [Speed 1].
    
## Files in "ans":  
  
 Each file is a set of solutions obtained by MT-SPlit algorithm. 
 
Each solution is composed by [N_vehilces, Travel Cost, [route split into trips],[each trip's departure time and arrival time].
> For example: [7, 2567.834968583103, [[0, 89, 47, 27, 79, 69, 62, 67, 0], [0, 95, 102, 37, 28, 68, 24, 45, 0], [0, 109, 0], [0, 87, 38, 48, 73, 57, 71, 83, 0], [0, 100, 92, 12, 88, 36, 31, 0], [0, 15, 11, 19, 93, 75, 7, 76, 4, 56, 17, 30, 3, 0], [0, 91, 43, 86, 94, 97, 0], [0, 13, 46, 2, 78, 85, 50, 20, 103, 0], [0, 60, 105, 80, 74, 0], [0, 22, 108, 29, 0], [0, 99, 25, 64, 9, 59, 70, 18, 65, 14, 0], [0, 96, 1, 63, 41, 77, 81, 35, 34, 0], [0, 61, 16, 33, 53, 5, 101, 55, 42, 58, 23, 0], [0, 10, 107, 90, 0], [0, 110, 0], [0, 6, 8, 106, 72, 40, 26, 0], [0, 98, 104, 84, 0], [0, 39, 32, 44, 21, 54, 82, 49, 52, 66, 51, 0]], [[180.0, 335.7030403602777], [335.83930649540383, 486.5244394468417], [180.39199110209677, 245.5466402265412], [250.12504289794447, 378.5439887445226], [378.65124985563364, 511.0541416776611], [511.37101235243324, 753.4645302485585], [180.0365950606753, 294.2271341386309], [294.48768089991177, 471.72063725286296], [181.08903968410542, 303.0486401680536], [303.1793042426607, 387.35917378075794], [387.416854662716, 537.0336337353285], [180.53448369628657, 352.73032342878315], [353.27871371297454, 533.0192520036724], [180.87294162921077, 280.2215419276168], [280.7243824257257, 342.66532398350347], [343.7087390227325, 501.4770920983486], [231.77803170277147, 331.9822069689412], [335.0014021645162, 539.9999999999997]]]

 Each name of file is "Number of customers"_("Fix cost of a vehicle", "Capcity", "Maximul travel distance of a trip")

> For example: 110_ (10,1000.0,1000.0).txt
