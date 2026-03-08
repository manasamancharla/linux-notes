# Process Management
A process is simply a program that is currently running on a system. When a command is executed or an application is opened, a process is started. Each process is uniquely identified by a Process ID (PID) assigned by the kernel.

## Viewing Processes

The `ps` ( process status ) command is used to display information about currently running processes.

### 1. `ps aux`
Displays detailed information about all running processes on the system.

#### Options Used

| Option | Description |
|-----|-------------|
| `a` | Shows processes for all users, not just the current user. |
| `u` | user-oriented format (verbose), also shows CPU and memory usage. |
| `x` | Shows processes that do not have a controlling terminal, such as background services or daemons. |

### 2. `ps -ef`
Displays processes in a full-format listing.

#### Options Used

| Option | Description |
|-----|-------------|
| `e` | Shows every process running on the system. |
| `f` | Shows full-format information about each process. |

### 3. `ps aux | grep process`
Finds a specific process

But a drawback is that it may also show the grep process itself. `ps aux | grep process | grep -v grep` avoids that.

### 4. `pgrep process`
Searches for processes by name and returns the Process IDs (PIDs).

## Managing Processes
- `kill PID` – Terminate a process by PID
- `pkill processname` – Terminate a process by name
- `kill -9 PID` – Force kill a process
- `kill -STOP PID` – Stop a running process
- `kill -CONT PID` – Resume a stopped process
- `nice -n [value] command` - Run a command with a nice value
- `renice -n 10 -p PID` – Lower priority of a process
- `renice -n -5 -p PID` – Increase priority of a process (requires root)

### Background & Foreground Processes
- `command &` – Run a command in the background
- `jobs` – List background jobs
- `fg %jobnumber` – Bring a job to the foreground
- `Ctrl + Z` – Suspend a running process
- `bg %jobnumber` – Resume a suspended process in the background



