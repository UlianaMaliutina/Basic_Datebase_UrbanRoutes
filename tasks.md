## The Console
# Task 1
1: Enter the command or sequence of commands that returned the required logs:
## grep -R "^233.201." ~/logs/2019/12

2: Show the results of your search:

/home/morty/logs/2019/12/apache_2019-12-18.txt:233.201.188.154 - - [18/12/2019:21:46:01 +0000] "DELETE /events HTTP/1.1" 403 3971

/home/morty/logs/2019/12/apache_2019-12-21.txt:233.201.182.9 - - [21/12/2019:21:56:20 +0000] "PATCH /users HTTP/1.1" 400 4118

# Task 2
1: Enter the commands you used to create the /bug1 and /events directories: 

mkdir ~/bug1
mkdir ~/bug1/events

2: Enter the commands you used to select logs for the specified periods. These are the requests that you use to select logs for the main.txt file:

ls ~/logs/2019/12
grep " [45]00 " ~/logs/2019/12/apache_2019-12-30.txt > ~/bug1/main.txt

3:  Enter the commands that you used to put logs from the main.txt file into the 400.txt and 500.txt files:

grep " 400 " ~/bug1/main.txt > ~/bug1/events/400.txt
grep " 500 " ~/bug1/main.txt > ~/bug1/events/500.txt

4: Show the results of your work, i.e. the contents of 400.txt and 500.txt. Since there will be many lines of text, provide a selection of the output, as below:


A: The line count of  400.txt. Use wc ~/bug1/events/400.txt to get the answer.
172  1720 13860 /home/morty/bug1/events/400.txt

B: The first 3 lines from 400.txt. Use head -3 ~/bug1/events/400.txt to get the answer.
80.57.170.51 - - [30/12/2019:21:35:12 +0000] "DELETE /users HTTP/1.1" 400 3623
204.235.176.118 - - [30/12/2019:21:35:13 +0000] "POST /users HTTP/1.1" 400 4704
82.95.203.67 - - [30/12/2019:21:35:19 +0000] "DELETE /lists HTTP/1.1" 400 3737

C: The last 3 lines from 400.txt. Use tail -3 ~/bug1/events/400.txt to get the answer.
203.106.235.105 - - [30/12/2019:22:12:38 +0000] "DELETE /events HTTP/1.1" 400 4158
18.211.28.150 - - [30/12/2019:22:12:40 +0000] "DELETE /collectors HTTP/1.1" 400 2212
229.16.123.45 - - [30/12/2019:22:12:54 +0000] "GET /auth HTTP/1.1" 400 2397

D: The line count of 500.txt. Use wc ~/bug1/events/500.txt to get the answer.
 156  1560 12554 /home/morty/bug1/events/500.txt

E: The first 3 lines from 500.txt. Use head -3 ~/bug1/events/500.txt to get the answer.
64.250.112.189 - - [30/12/2019:21:35:13 +0000] "PUT /parsers HTTP/1.1" 500 4639
193.253.101.180 - - [30/12/2019:21:35:31 +0000] "PATCH /alerts HTTP/1.1" 500 2944
197.106.117.194 - - [30/12/2019:21:35:31 +0000] "PATCH /parsers HTTP/1.1" 500 3519

F: The last 3 lines from 500.txt. Use tail -3 ~/bug1/events/500.txt to get the answer.
207.6.210.203 - - [30/12/2019:22:12:37 +0000] "PATCH /events HTTP/1.1" 500 4298
33.13.118.148 - - [30/12/2019:22:12:38 +0000] "PUT /alerts HTTP/1.1" 500 4711
107.188.33.199 - - [30/12/2019:22:12:59 +0000] "POST /parsers HTTP/1.1" 500 2833

## Databases
# Task 3
Please specify the number of cars: 5500
The query that you used to find the number of cars:

SELECT COUNT(DISTINCT vehicle_id) AS car_numb FROM cabs;

# Task 4
List of companies with fewer than 100 cars:
                 company_name                 | cnt
----------------------------------------------+-----
 Nova Taxi Affiliation Llc                    |  97
 Patriot Taxi Dba Peace Taxi Associat         |  89
 Blue Diamond                                 |  85
 Checker Taxi Affiliation                     |  81
 Chicago Medallion Management                 |  80
 Chicago Independents                         |  69
 24 Seven Taxi                                |  67
 Checker Taxi                                 |  60
 American United                              |  55
 Chicago Medallion Leasing INC                |  53
 Top Cab Affiliation                          |  49
 KOAM Taxi Association                        |  48
 Chicago Taxicab                              |  38
 Norshore Cab                                 |  34
 Gold Coast Taxi                              |  20
 Metro Group                                  |  20
 Service Taxi Association                     |  18
 5 Star Taxi                                  |  14
 American United Taxi Affiliation             |   8
 Metro Jet Taxi A                             |   8
 Setare Inc                                   |   7
 Leonard Cab Co                               |   5
 4615 - 83503 Tyrone Henderson                |   1
 5062 - 34841 Sam Mestas                      |   1
 4623 - 27290 Jay Kim                         |   1
 5997 - 65283 AW Services Inc.                |   1
 2092 - 61288 Sbeih company                   |   1
 1469 - 64126 Omar Jada                       |   1
 2733 - 74600 Benny Jona                      |   1
 2192 - 73487 Zeymane Corp                    |   1
 5006 - 39261 Salifu Bawa                     |   1
 3556 - 36214 RC Andrews Cab                  |   1
 3721 - Santamaria Express, Alvaro Santamaria |   1
 2809 - 95474 C & D Cab Co Inc.               |   1
 2241 - 44667 - Felman Corp, Manuel Alonso    |   1
 3620 - 52292 David K. Cab Corp.              |   1
 2823 - 73307 Lee Express Inc                 |   1
 6057 - 24657 Richard Addo                    |   1
 6742 - 83735 Tasha ride inc                  |   1
 1085 - 72312 N and W Cab Co                  |   1
 3591 - 63480 Chuks Cab                       |   1
 0118 - 42111 Godfrey S.Awir                  |   1
 6574 - Babylon Express Inc.                  |   1
 3094 - 24059 G.L.B. Cab Co                   |   1
 5874 - 73628 Sergey Cab Corp.                |   1
 6743 - 78771 Luhak Corp                      |   1
 5074 - 54002 Ahzmi Inc                       |   1
 3623 - 72222 Arrington Enterprises           |   1
 4053 - 40193 Adwar H. Nikola                 |   1
 Chicago Star Taxicab                         |   1
 3011 - 66308 JBL Cab Inc.                    |   1

The query that you used to generate the list of companies above:
SELECT company_name, COUNT(vehicle_id) AS cnt FROM cabs GROUP BY company_name HAVING COUNT(vehicle_id) < 100 ORDER BY cnt DESC;
