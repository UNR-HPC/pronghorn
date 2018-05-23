### This script is written to take a Gaussian input file as an argument.  It will dump its output into the directory from which it was invoked.  The following are some use cases for this script:

### Notes:
* This Script will run 16 core jobs on up to 112GB of memory
* Please ensure your input files are set for 16 cores using %NProcShared=16.
* CPU affinity cannot be used with this script at this time.


### Simple invocation
script will be executed from the current working directory
input file will be read from the current working directory
output to the current working directory
> $ sbatch rc-g16-0.sl input.gjf

### Invoke script from a shared location
script will be executed from an installation directory
input file will be read from the current working directory
output to the current working directory
> $ sbatch /path/to/script/rc-g16-0.sl input.gjf

### Everything variable
script will be executed from an installation directory
input file will be read from an input directory
output to the current working directory
> $ mkdir output
> $ cd output
> $ sbatch /path/to/script/rc-g16-0.slrc-g16-0.sl /path/to/input/input.gjf

### Change run time from command line
no need to edit the script to change sbatch parameters
> $ sbatch --time=10-00:00:00 rc-g16-0.sl input.gjf

### Set an email for notification on job state change from command line
> $ sbatch --mail-user=<netid>@unr.edu rc-g16-0.sl input.gjf

#### Change the job name and run time from the command line
> $ sbatch --job-name=myjob --time=02:00:00 rc-g16-0.sl input.gjf

