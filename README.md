# python-cf-tasks
Examples of using Cloud Foundry tasks in Python

## Simple Print task
```
$ cd 01-simple_print
$ cf push
$ cf run-task ih-printer 'python printer.py' --name print-now
```

The expected outcome in the logs (`cf logs ih-printer --recent`) is something like
```
   2017-07-22T12:01:29.64+0100 [CELL/0] OUT Creating container
   2017-07-22T12:01:30.27+0100 [CELL/0] OUT Successfully created container
   2017-07-22T12:01:33.39+0100 [APP/TASK/print-now/0] OUT Hello, I'm the task you requested.
   2017-07-22T12:01:38.39+0100 [APP/TASK/print-now/0] OUT Beep Boop Bing.
   2017-07-22T12:01:43.40+0100 [APP/TASK/print-now/0] OUT Your task is now complete!
   2017-07-22T12:01:43.40+0100 [APP/TASK/print-now/0] OUT Exit status 0
   2017-07-22T12:01:43.41+0100 [CELL/0] OUT Destroying container
   2017-07-22T12:01:44.27+0100 [CELL/0] OUT Successfully destroyed container
```
