# Install 

`teos_cli` has some dependencies that can be satisfied by following [DEPENDENCIES.md](DEPENDENCIES.md). If your system already satisfies the dependencies, you can skip that part.

There are two ways of running `teos_cli`:  running it as a module or adding the library to the PYTHONPATH env variable.

## Running `teos_cli` as a module
The **easiest** way to run `teos_cli` is as a module. To do so you need to use `python -m`. From `cli` **parent** directory run:

    python -m cli.teos_cli -h
    
Notice that if you run `teos_cli` as a module, you'll need to replace all the calls from `python teos_cli.py <argument>` to `python -m cli.teos_cli <argument>` 

## Modifying `PYTHONPATH`
**Alternatively**, you can add `teos_cli` to your `PYTHONPATH` by running:

	export PYTHONPATH=$PYTHONPATH:<absolute_path_to_cli_parent>
	
For example, for user alice running a UNIX system and having `python-teos` in her home folder, she would run:
	
	export PYTHONPATH=$PYTHONPATH:/home/alice/python-teos/
	
You should also include the command in your `.bashrc` to avoid having to run it every time you open a new terminal. You can do it by running:

	echo 'export PYTHONPATH=$PYTHONPATH:<absolute_path_to_cli_parent>' >> ~/.bashrc
	
Once the `PYTHONPATH` is set, you should be able to run `teos_cli` straightaway. Try it by running:

	cd <absolute_path_to_cli_parent>/cli
	python teos_cli.py -h
	

## Modify configuration parameters
If you'd like to modify some of the configuration defaults (such as the user directory, where the logs and appointment receipts will be stored) you can do so in the config file located at:

	 <data_dir>/.teos_cli/teos_cli.conf
	 
`<data_dir>` defaults to your home directory (`~`).
