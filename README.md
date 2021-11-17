# TABLEAU-AIRPORT-PROJECT
We create a Dashboard to display the San Francisco Airport Details. We make use  concept of Calculated Fields, Filters  and other important visual charts to explain our Dashboard


## Create Important KPIs for the Dashboard  ( KEY PERFORMANCE INDICATORS)

1)  Number of Flights -  By use of Calculated Field

![1](https://user-images.githubusercontent.com/34785563/142210736-a8291d90-64f9-4552-8c3a-487c40927e4a.png)

      
2) Number of Flights per Day ( Trend line information )
    
    
    ROWS -  DAY(DATE)
    COLUMNS - NUMBER OF FLIGHTS
    
![2](https://user-images.githubusercontent.com/34785563/142211130-27ee494b-59eb-4ac4-be1a-045068ac10c0.png)
 
 
3) Most Pouplar DAY
![image](https://user-images.githubusercontent.com/34785563/142211426-e604cf2b-ab77-4bad-a61e-6c2eab6db283.png)

4) ROUTES

  We create  a Calculated Field- Grouped Routed to remove the effect of SFO Airport
  
  GROUPED ROUTE = if [Route -  1]='SFO' THEN [Route -  2] ELSE [Route -  1] END
  
  We create a chart ROWS- GROUPED ROUTE 
                    COLUMNS- SUM(Number of Records)
                    
                    We create a Filter such that we filter only Top 5 records
  
  ![4](https://user-images.githubusercontent.com/34785563/142212189-d05653ca-a403-4ecb-85cd-6360066b7a2b.png)


5) DISTANCE

  We created FROM  and TO  using Calculated Fields  use of Make point function 
  
    FROM  - MAKEPOINT([Geometry Coordinates 1 1],[Geometry Coordinates 1 0])
    
    TO-  MAKEPOINT([Geometry Coordinates 0 1],[Geometry Coordinates 0 0])
    
    DISTANCE- DISTANCE([From],[To],'km')
    
    We create a Filter -TOP 5 AVERAGE DISTANCES
    
    
![5](https://user-images.githubusercontent.com/34785563/142212734-94908fbb-eb49-4091-9c1c-0d34e4681cec.png)

6) LINE


 We create Line using Calculated Field
 
    LINE- MAKELINE([From],[To])
![6](https://user-images.githubusercontent.com/34785563/142261812-67e8cb83-4689-4d31-b4e8-f53913352738.png)

    
## SAN FRANSISCO DASHBOARD

![7](https://user-images.githubusercontent.com/34785563/142261948-2a79bbac-6bfc-427a-8603-a30377a0df22.png)

