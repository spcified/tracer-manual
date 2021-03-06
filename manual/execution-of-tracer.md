# Execution of TRACER

Once all properties and parameters in `tracer_config.xml` are set, open the terminal and navigate to the TRACER folder \(using the command `cd`\). To start TRACER, type:

```text
java -Xmx600m -Deu.etrap.medusa.config.ClassConfig=conf/tracer_config.xml -jar tracer.jar > FILENAME.OUT
```

What does this command do? Let's break it down:

* `java` opens a Java programme.
* `-Xmx600m` defines the amount of memory to be used for the detection. In this case, the computation is set to use up to 600 MB memory. If you work on large data-sets and your computer supports it, you might have to raise this parameter to `1g`\(=1GB\), `2g`\(=2GB\) or more.
* `-Deu.etrap.medusa.config.ClassConfig=conf/tracer_config.xml` calls the TRACER configuration file.
* Optionally, you can add `-Dfile.encoding` to this command \(after `-Xmx600m`\) to set the encoding of your input file. This is important because operating systems use different default encoding. To set the character encoding to a Unicode standard, add `-Dfile.encoding=UTF-8` to the command.
* `FILENAME.OUT`. This file can be given any name \(e.g. `detection-task-1.out` or `results.out,` where out stands for _output_\) and will document the entire detection process. This file is useful to have in case the detection process is not successful. In these cases, the file will show where the TRACER process stopped allowing the user to try and locate the source of the error. The `.out` file is stored in the main `TRACER` folder. Printing the TRACER output in a `FILENAME.out` is optional; if you don't do it, the output of TRACER will be printed in the main command line screen.

Press `ENTER` and TRACER will perform a first text reuse detection task. The speed of the first run will depend on the memory of your computer but it generally takes a few minutes. When TRACER is done, you should see the screen below:

![](../.gitbook/assets/first-run.png)

If TRACER has not reached the end of Process Level 6 \(which is the _Postprocessing_ level\), then something in your detection run has gone wrong. The [Troubleshooting](../support/troubleshooting/) section of this GitBook contains a list of potential error sources.

