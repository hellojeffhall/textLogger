# textLogger
A bash script for logging to a text file.

You can call it with the following flags:

	--help or -h: (optional)
		Show this message.

	--path or -p: (optional)
		The path to the logfile that this should append to.
		Defaults to a file called "log" in the current directory.

	--service or -s:
		The name of the service submitting an entry.

	--level or -l:
		The logging level. (e.g., error, warning, info).

	--message or -m:
		Human-readable message for this log entry.

	--data or -d: (optional)
		Supplimental data related to this log entry 
		(e.g., JSON or a URI).

Log syntax:

    server_time|service|level|message|data

Input Examples:

    --service someAPI --level error --message "Invalid JSON" --data "{OK:no}"
    --service myApp --level warning -m "Only 4.3 GB left on disk."
    -s myApp -l info -m "User 728 deleted item 728."

Output Examples:

    2017-12-20 16:46:31 EDT|someAPI|error|Invalid JSON|{OK:no}
  	2017-12-20 16:48:17 EDT|myApp|warning|Only 4.3 GB left on disk.|
    2017-12-20 16:52:21 EDT|other app|info|User 728 deleted item 728.|

