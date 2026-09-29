DATA ENGINEERING EXAM PRACTICE DATASET
============================================

Files:
- customers.csv
- drivers.csv
- rides.csv
- ratings.csv
- payment_methods.csv
- queue_messages.jsonl
- events.db

Suggested Spark setup:
spark = SparkSession.builder.master("local[*]").appName("ExamPractice").getOrCreate()

Module 4:
The JSONL file simulates a queue. events.db contains the target table ride_events.
For practice, write a function that reads the next queue record(s), waits 60 seconds
between reads, stops when total execution time exceeds 60 seconds, parses JSON, and
inserts each record into ride_events. During practice you can replace sleep(60) with
sleep(2) while debugging.
