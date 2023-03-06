# Readers-Writers

This algorithm makes sure that whenever there is a writer,writers and readers follow first cum first serve fashion to complete their task.
And when there are no writers,all the readers will be able to read.

Semaphores and integers used:
x-(initialized to 1)-adds processes to the process queue when there are writers.
s-(initialized to 1)-used to ensure mutual eclusion of execution of writers.
mutex-(initialized to 1)-used to ensure mutual exclusion while updating rc.
rc-(initialized to 0)-used to keep track of the number of reader process being executed.

When there are no writers,all the reader processes can perform read.
When a write process enters,X semaphore makes sure that the write process enters the process queue and processes are performed one after another.
When there are only writers and a reader process enter,S semaphore make sure that the reader enter the process queue and the processes execute one after other.
mutex semaphore ensures mutual exclusion while updating rc.
rc is to count the number of reader processes being executed.
