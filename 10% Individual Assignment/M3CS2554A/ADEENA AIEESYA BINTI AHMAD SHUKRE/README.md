# Airport Baggage Handling and Sorting Simulator

**NAME:** ADEENA AIEESYA BINTI AHMAD SHUKRE

**STUDENT ID:** 2024648084

**CLASS:** M3CS2554A

**COURSE CODE:** ITT440 Network Programming

**YOUTUBE LINK:** 

-------------------------------------------------------------------------------------------


## PROBLEM STATEMENT
In the context of airport baggage handling, where thousands or even millions of records may need to be processed, selecting the most efficient processing method becomes critical.

While the sequential processing provides a simple approach, it may not be suitable for handling large volumes of data efficiently. To overcome this issue, concurrency and parallelism are introduced in modern computing. Concurrent programming allows several tasks to be managed at once, improving system responsiveness, while parallel programming allows tasks to be executed simultaneously across various CPU cores, improving performance for computationally demanding workloads.

Thus, this project focuses on evaluating and comparing three processing techniques, which are sequential, concurrent, and parallel processing by simulating a large scale airport baggage handling system. The aim is to identify which approach provides better performance and scalability when handling large datasets.


## SYSTEM DESIGN
First, the system generates baggage data automatically based on user input. Each baggage record contain basic information such as bag ID, weight, destination, priority, and complexity level. The use of automatically generated data allows the system to simulate large scale situations without requiring manual input.

Next, the system processes the generated data using three different techniques. In sequential processing, each baggage record is processed one by one. In concurrent processing, multiple threads are used to process baggage records simultaneously by retrieving tasks from a shared queue. In parallel processing, multiple processes are created using a process pool, where each process handles part of the workload independently.

The system measures the execution time for each processing method using a timer. This allows a direct comparison of performance between the three approaches. After processing is complete, the system displays a summary of results, including the number of baggage items processed and the total workload score.


## SYSTEM REQUIREMENTS
To run the Airport Baggage Handling and Sorting Simulator, the system requirements needed are : 
- Operating System : Windows, Linux (Kali), or macOS
- Python Version : Python 3.8 or above
- Processor : Multicore CPU
- RAM : Minimum 4GB, but the bigger the better as the dataset that will be handled are massive.
- Storage : At least 1GB free space
- Terminal : Required to run the program


## INSTALLATION STEPS

***A. LAUNCH THE SIMULATOR***

**Navigate to project folder**

```bash
cd airport_baggage_sim
```

**Run the program**

```bash
python3 airport_main.py
```

***B. PROVIDE DESIRED INPUT***

**When prompted, enter the required values, for example:**

```bash
Enter number of baggage records (example: 1000000): 100000
Enter number of threads: 4
Enter number of processes: 4
```

***C. SYSTEM EXECUTION***

**The program will automatically:**

```bash
- Generate large-scale baggage data automatically
- Execute sequential processing (baseline method)
- Execute concurrent processing using threading
- Execute parallel processing using multiprocessing
- Measure and record execution time for each method
- Analyze baggage distribution across destinations
- Identify busiest and least busy destinations
- Calculate total processing load and average load per bag
- Display a summarized analytics report
- Compare performance and identify the fastest method
```



## SAMPLE OUTPUT

```bash
========== BAGGAGE ANALYTICS REPORT ==========

Baggage distribution:
KUL: 16654 bags (16.65%)
JHB: 16713 bags (16.71%)
PEN: 16621 bags (16.62%)
LGK: 16678 bags (16.68%)
BKI: 16658 bags (16.65%)
KCH: 16676 bags (16.68%)

Total baggage processed: 100000

Busiest destination: JHB (16713 bags)
Least busy destination: PEN (16621 bags)

Total processing load: 1532849210
Average load per bag: 15328

========== PERFORMANCE ==========
Sequential      : 8.5000s
Threading       : 6.9000s
Multiprocessing : 3.2000s
Fastest Method  : Multiprocessing
```


## ANALYTIC
| Destination               | Number of Bag  | 
|---------------------------|----------------| 
| KUL                       | 4 568 bags    | 
| JHB                       | 4,568 bags    | 
| PEN                       | 4,568 bags    | 
| LGK                       | 2,284 bags    | 
| BKI                       | 2,284 bags    | 
| KCH                       | 2,284 bags    |
| **Total Processing Load** | **18,272**     |




## CONCLUSION
In conclusion, this project successfully developed an airport baggage handling and sorting simulator using Python to process large scale data efficiently. The system implemented three different processing techniques, which are sequential processing, concurrent processing using threading, and parallel processing using multiprocessing, to simulate real world scenarios when a huge amount of baggage records must be handled. The results demonstrated that sequential processing, although simple, becomes inefficient as the dataset size increases due to its one by one execution approach. Threading provided some improvement by allowing tasks to be handled concurrently, but its performance remained limited for CPU intensive operations.

On the other hand, multiprocessing achieved the best performance among all techniques by utilizing multiple CPU cores, enabling true parallel execution and significantly reducing processing time for large datasets. This shows that parallel processing is the most suitable approach for handling large-scale and computationally intensive tasks such as airport baggage handling systems. Overall, the project highlights the importance of selecting the appropriate processing method based on the nature of the workload and demonstrates how concurrency and parallelism can improve efficiency and scalability in practical applications.




