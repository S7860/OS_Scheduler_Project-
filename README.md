# Improve Process scheduling in Linux using Machine Learning #

In this project we created a data set which can be used to implement
Machine Learning Model. The goal was to use previous execution history
of processes and utilize it to recognize a program and predict it resource requirement. This will reduce the idle time and improve
efficiency of processes and Processor.

# Data Set #
There were 4 processes created and two types of data collected on them.<br />
**Static Data** - Total of 8 process attributes were collected upon completion of the process using wait4()
system call.
**Dynamic Data** - Collected by reading the /proc file system maintained by the OS.

# Dynamic Data Attributes #
**exec_start** - the process was started. <br/>
**vruntime** - Virtual run time. <br/>
**sum_exec_runtime** -  CPU time  (utime + stime). <br/>
**nr_migrations** - No. of time process was switch to a different CPU. <br/>
**load_weight** - Calculated using the priority. This value helps in generating the time slice given to the process.<br/>
**rchar** - It is I/O counter chars read. <br/>
This is simply the sum of bytes which this process passed to read() and pread().<br/>
**wchar** - the number of bytes which this task has caused, or shall cause to be written to disk.
**syscr** - Attempt to count the number of read I/O operations.<br/>
**syscw** - Attempt to count the number of write I/O operations. <br/>
**read_bytes** - Attempt to count the number of bytes which this process cause to be fetched from the storage layer. <br/>
**write_bytes** - Attempt to count the number of bytes which this process caused to be sent to the storage layer.<br/>

### Side Note on the file_rw folder ###
Since the output for that file was very large due to it we were unable to upload it. However, to see the behaviour of the process code simply run **.c** file.
