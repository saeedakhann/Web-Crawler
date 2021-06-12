
Saeeda Khan 17L-6307

*******************************Main********************************** 
For loop contains loop to create multiple threads and each thread calls
"reapeatFunction()" which looks at the size of Crawled URL array and calls
"crawler_thread_task()" reapeatedly till its size < 1000
********************************************************************* 

****************crawler_thread_task()********************************** 
The crawler_thread_task() function 
1. Checks if any back queue is empty calls "add_to_backqueue()".
2. Then it calls "get_URL()" which returns back queue number
   which has not been accessed for maximum amount of time.
3. Last Access time for that array is checked if less than 15
   thread sleeps and waits till last accessed is greater than 15 seconds
4. URL is removed from back queue 
5. Last Access time of queue is updated
6. Extracted URL is processed by fetching its content, extracting links,
   filter using robot.txt, and removing duplicates
7. Resultant URL's are added to Front queues
***********************************************************************
Each URL that is crawled its content is saved in a separate XML example1.xml,
example2.xml