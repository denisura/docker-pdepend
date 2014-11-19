docker-pdepend
==============

Run PHP Depend tool (pdepend) in Docker container. This tool shows you the quality of your design in the terms of extensibility, reusability and maintainability.  http://pdepend.org


docker-phpab
============

Run PHP Autoload Builder (phpab) in Docker container

Build
--------------------

Build from `Dockerfile`:

    ``` sh
    sudo docker build  -t denisura/pdepend .
    ```

Verify build:

    ``` sh
    sudo docker run --rm -it denisura/pdepend --version
    ```

Usage
--------------------

1. Install the `denisura/pdepend` container (optional - this step is performed by Docker automatically when running the container):

    ``` sh
    $ docker pull denisura/pdepend
    ```

2. Define an bash alias that runs this container whenever `pdepend` is invoked on the command line:

	``` sh
	$ echo "alias pdepend='docker run --rm -it -v \$(pwd):/workspace denisura/pdepend'" >> ~/.bashrc
	$ source ~/.bashrc
	```

3. Run phpunit as always:

	``` sh
	$ pdepend --version
	```