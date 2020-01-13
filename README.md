## My Flask-Bootstrap Playground 
> Pretest for some features to implement on virtual machine

- Single line display ```Completed```
  - Modified fieldmergeList of waiver
- RPTlink ```Completed```
  - Added selecting waiver branch to /app/main_fcnl/common/tablepainter_q.py
  - Maintained front-end html funtion RPTlink at templates/supra/tablepainter_qor.html
- Username
  - In python, all shell scripts (os.system(cmd)) will return a status code after its execution. To correctly get the stdout, below is the way. 
  ```
  from subprocess import PIPE, Popen
  def cmdline(command):
      process = Popen(
          args=command,
          stdout=PIPE,
          shell=True
      )
      return process.communicate()[0]

  print cmdline("cat /etc/services")
  print cmdline('ls')
  print cmdline('rpm -qa | grep "php"')
  print cmdline('nslookup google.com')
  ```
  - Another solution also works fine on my personal pc
  ```
  import subprocess

  proc = subprocess.Popen(["cat", "/etc/services"], stdout=subprocess.PIPE, shell=True)
  (out, err) = proc.communicate()
  print "program output:", out
  ```
- workflow
