To add test alarm-mega:

Use grep -r alarm-multiple to find where this file is referenced.
Add extern test_func test_alarm_mega; to tests.h
Add {"alarm-mega", test_alarm_mega}, to tests.c
Add 
test_alarm_mega (void) 
{
  test_sleep (5, 100);
}
to alarm-wait.c
Go to pintos/src/threads and make clean then make
Run test to log file by using command: pintos –v -- run  alarm-mega 
> log-mega.txt