
## .deb file is the installation file in `Linux` system

### Steps:
1. cd to the file directory
2. install the package use
	```sh
    sudo dpkg -i xxx.dep
    ```
	
	If you encounter dependency errors, run this:
    ```bash
    sudo apt-get -f install  [Not tested]
    ```
	
	
3. It's done, run 
	```bash
    code    // to launch visual stodio code.
    ```