###########
Quick Start
###########

You must be logged in to load or save waves.

.. _loading-waves-from-playground:

*********************************
Loading Waves from EDA Playground
*********************************

You can run a simulation on EDA Playground and load the resulting waves in EPWave.

* Go to your code on EDA Playground. For example: `RAM Design and Test <http://www.edaplayground.com/s/example/9>`_
* Make sure your code contains appropriate function calls to create a \*.vcd file. For example:

  .. code-block:: verilog

     initial begin
       $dumpfile("dump.vcd");
       $dumpvars(1);
     end
  
* Select a simulator and check the **Open EPWave after run** checkbox. (Not all simulators may have this run option.)

  .. image:: _static/openEpwaveCheckbox.png

* Click **Run**. After the run completes, the resulting waves will load in a new EPWave window. (Pop-ups must be enabled.)

.. _loading-waves-from-file-url:

******************************
Loading Waves from File or URL
******************************

* On `EPWave Homepage <http://www.edaplayground.com/w/home>`_, specify the wave dump file to load. There are 2 sources for loading waves.

  #. Specify the URL pointing to the waves accessible over the web, such as a file in a public Dropbox folder.
  #. Upload the wave dump from your own computer.
  
* After specifying the wave dump file, you can click the **Load** button to load the waves.
  
* If your wave dump contains 2000 signals or larger, you may specify a *Signal Filter* so that fewer than 2000 signals are loaded.
  If *Signal Filter* is not specified, then only the first 2000 signals will be loaded.
  Click on the **+** on the top left to open the *Signal Filter*. For \*.vcd files, the filter accepts regular expressions.

  .. image:: _static/signal_filter.png
  
  After specifying the *Signal Filter*, click the **Load** button to load the waves.

* (Optional) You may specify the *From* and/or *To* times to limit the time range of the loaded wave.
  If your wave dump contains a lot of data, then the ending *To* time will automatically be limited.
  
  .. image:: _static/from_to.png

***************
Viewing Signals
***************

After loading the waves, you can display signals by using the **Get Signals** button.

.. image:: _static/get_signals.png
