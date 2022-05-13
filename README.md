# signa-handling-code-in-command-line
This code uses sygnal to count  the number of loops  and execution time when CTRL+ C signal is sent
/*

Toxicking_Techguru

*/

#include <stdio.h> 
#include <stdlib.h> 
#include <signal.h> 
#include <unistd.h>
#include <time.h>
void handler2(int num)//second signal handler 
{
int tick = clock();
printf(" %f seconds is the total time of  execution \n",(float)tick / CLOCKS_PER_SEC * 1000);
exit(1);

}

void handler(int signum)// first signal handler
{
    printf("Hello World!\n");
    alarm(1);//Schedule a SIGALRM for a second
}
 /*

Toxicking_Techguru

*/
int main()
{
signal (SIGALRM, handler);//register handler to handle SIGALRM
signal (SIGINT,handler2);//register handler to handle SIGALRM
signal (SIGTERM,handler);//tells the program to terminate itself 
    alarm(1);//Schedule a SIGALRM for 1 second
    while(1) {
        sleep(1);//waiting for signal to be delivered
        printf("Turing was right\n");
       
    }
    ggjjjjjjjgg
    
    ffrg
    zgrfz
    
    gf
    gfr
    
    
    return 0;
}
