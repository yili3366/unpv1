BIN = client serv01 serv02 serv03 serv04 serv05 serv06 serv07 serv08

CFLAGS = -g -gdwarf-4 -Wall
LDFLAGS = ../libunp.a -I ../include -lpthread

all: $(BIN)

client : client.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

serv01 : pr_cpu_time.c web_child.c sig_chld.c serv01.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

serv02 : pr_cpu_time.c web_child.c sig_chld.c child02.c serv02.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

serv03 : pr_cpu_time.c web_child.c sig_chld.c child03.c lock_fcntl.c serv03.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

serv04 : pr_cpu_time.c web_child.c sig_chld.c child04.c lock_fcntl.c serv04.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

serv05 : pr_cpu_time.c web_child.c sig_chld.c child05.c lock_fcntl.c serv05.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

serv06 : pr_cpu_time.c web_child.c sig_chld.c child05.c lock_fcntl.c serv06.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

serv07 : pr_cpu_time.c web_child.c pthread07.c  serv07.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

serv08 : pr_cpu_time.c web_child.c pthread08.c  serv08.c
	$(CC) $(CFLAGS) $? $(LDFLAGS) -o $@

.PHONY: clean
clean:
	rm $(BIN)
