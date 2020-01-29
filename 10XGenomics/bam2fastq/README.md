# bamtofastq

A Docker container recipe for the 10X Genomics program bamtofastq based on [the official github repo](https://github.com/10XGenomics/bamtofastq).

The container has a Fedora linux base. One way to run bamtofastq is like this:

`docker run -it sgivan/bamtofastq bamtofastq -h`

Within the container, the files for the bamtofastq github repo are in `/bamtofastq`. So, to run a test to see if bamtofastq is working, you can use one of the test files included in the repo. You will also probably need to mount a directory from your local file system into the container. Something similar to this should work:

`docker run -v /full/path/on/local/filesystem/outputDirectory:/mnt/outputDirectory sgivan/bamtofastq bamtofastq /bamtofastq/test/lr21.bam /mnt/outputDirectory/run1`

The output files should be in `/full/path/on/local/filesystem/outputDirectory/run1`.


