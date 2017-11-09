#include <stdio.h>
#include <stdlib.h>
#include <signal.h>
#include <unistd.h>

static void sighandler(int signo) {
    if (signo == SIGINT) {
        printf("ahhhhhhhhhhhhhhhhhhhhhhhhhhhhhhh\n");
        exit(1);
    }

    if (signo == SIGUSR1) {
        printf("parent process pid: %d\n", getppid());
    }
}

int main() {

  signal(SIGINT,sighandler);
  signal(SIGUSR1,sighandler);

  while(1) {
    printf("signal.c PID: %d\n",getpid());
    sleep(1);

  }
}
