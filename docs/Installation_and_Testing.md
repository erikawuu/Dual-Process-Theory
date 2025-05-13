## **Dependencies**

To use the Flee code, one requires:

* Python 3 interpreter (3.7 or higher)
* Python libraries
	- numpy (see [https://www.numpy.org](https://www.numpy.org))
	- pandas (see [https://pandas.pydata.org](https://pandas.pydata.org))
	- matplotlib (see [https://matplotlib.org](https://matplotlib.org))
	- scipy (see [https://scipy.org](https://scipy.org))
	- folium (see https://python-visualization.github.io/folium/)
	- ipython (see https://ipython.org)
* [git](https://git-scm.com/docs/git) needs to be installed in your machine.
* [mpirun](https://www.open-mpi.org/) needs to be installed in your machine.


## **Installing Flee**

To install Flee on your local workstation, you need to 

1. Clone the Flee repository:
	```sh
	git clone https://github.com/djgroen/flee.git
	```
	Once cloning completes, Flee will appear in your working directory as `<current dir>/flee`.

2. Open the appropriate configuration file:
	- For Linux users and Mac users with a bash shell (default for many Linux distributions):
	```sh
	vim ~/.bashrc
	```
	- For Mac users using zsh (the default shell on macOS Catalina and later):
	```sh
	vim ~/.zshrc
	```

3. Add the following line to the end of the file:
	```sh
	export PYTHONPATH=<path to flee>:$PYTHONPATH
	```
4. Save and close the file, then reload the configuration:
	- For bash:
	```sh
	source ~/.bashrc
	```
	- For zsh:
	```sh
	source ~/.zshrc
	```

## **Updating Flee**

If you have already installed Flee and want to update to the latest version, in your local Flee directory simply type

```sh
git pull
```

## **Testing Flee**

To run the basic tests, simply type

```sh
cd flee
pytest tests/
```

If you have FabFlee installed, then you can also run the FabFlee tests. To prepare for this, go to your main Flee directory and create a symbolic link using:

```sh
ln -s <main FabFlee directory> FabFlee
```

After that, you can then perform the tests using `pytest tests_mpi`.


Lastly, to do a simple single test run, use `python3 tests/test_csv.py`.
