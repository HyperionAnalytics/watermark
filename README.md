watermark
=========

An IPython magic extension for printing date and time stamps, version numbers, and hardware information.

**This is a fork with following enhancements:**
* Show system info as OS X version number or Linux distribution name
* Show release info as OS X or Linux kernel version
* Show processor info as manufacturer and CPU name, and clock frequency
* Show Intel MKL version if installed

<br>
#### Contents

- [Examples](#examples)
- [Installation and updating](#installation-and-updating)
- [Usage](#usage)


<br>
<br>

## Examples
[[back to contents](#contents)]

	%watermark

	04/12/2014 07:46:48

	CPython 3.4.2
	IPython 2.3.1

	compiler   : GCC 4.2.1 (Apple Inc. build 5577)
	system     : OS X 10.10.1
	release    : 14.0.0
	machine    : x86_64
	processor  : Intel(R) Core(TM) i7-3740QM CPU @ 2.70GHz
	CPU cores  : 8
	interpreter: 64bit

<br>

	%watermark -v -m -p numpy,scipy,mkl

	CPython 3.4.2
	IPython 2.3.1

	numpy 1.9.1
	scipy 0.14.0
	mkl 11.1.1

	compiler   : GCC 4.2.1 (Apple Inc. build 5577)
	system     : OS X 10.10.1
	release    : 14.0.0
	machine    : x86_64
	processor  : Intel(R) Core(TM) i7-3740QM CPU @ 2.70GHz
	CPU cores  : 8
	interpreter: 64bit

For more examples can be found in this [IPython notebook](http://nbviewer.ipython.org/github/rasbt/watermark/blob/master/docs/watermark.ipynb).

<br>
<br>

## Installation and updating
[[back to contents](#contents)]

In order to intall `watermark`, execute the the following code snippet in an IPython shell or IPython notebook cell.

	%install_ext https://raw.githubusercontent.com/HyperionAnalytics/watermark/master/watermark.py

For updates, simply execute the `%install_ext` again. Information about the current watermark version can be found in the help menu (via `%watermark?`).

<br>
<br>

## Usage
[[back to contents](#contents)]

After successful installation, the `watermark` magic extension can be loaded via:

	%load_ext watermark

<br>
<br>

To get an overview of all available commands, type:

	%watermark?

<br>



	%watermark [-a AUTHOR] [-d] [-n] [-t] [-z] [-u] [-c CUSTOM_TIME] [-v]
	                 [-p PACKAGES] [-h] [-m] [-g]


	IPython magic function to print date/time stamps
	and various system information.

	watermark version 1.1.0

	optional arguments:
	  -a AUTHOR, --author AUTHOR
	                        prints author name
	  -d, --date            prints current date
	  -n, --datename        prints date with abbrv. day and month names
	  -t, --time            prints current time
	  -z, --timezone        appends the local time zone
	  -u, --updated         appends a string "Last updated: "
	  -c CUSTOM_TIME, --custom_time CUSTOM_TIME
	                        prints a valid strftime() string
	  -v, --python          prints Python and IPython version
	  -p PACKAGES, --packages PACKAGES
	                        prints versions of specified Python modules and
	                        packages
	  -h, --hostname        prints the host name
	  -m, --machine         prints system and machine info
	  -g, --githash         prints current Git commit hash

