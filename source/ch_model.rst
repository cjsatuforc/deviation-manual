.. model menu

.. role:: subi
    :class: subscript-italic

.. |S0| replace:: *Switch*\ :subi:`0` 
.. |M0| replace:: *M*\ :subi:`0` 
.. |Sn| replace:: *Switch*\ :subi:`n` 
.. |Mn| replace:: *M*\ :subi:`n` 
.. |Sn-1| replace:: *Switch*\ :subi:`n-1` 
.. |Mn-1| replace:: *M*\ :subi:`n-1` 

.. _model-menu:

Model menu
==========

The model menu allows selection, editing model configuration, alarms, logging and screen configurations. You can access the menu by pressing the ENT key to select the 'Main menu' and then again on 'Model menu'.

Depending on the selection you have done for the Mixer GUI in section :ref:`model-setup`, the model menu operation will be completely different.

.. if:: devo10

The Advanced '2. Mixer' page (:ref:`mixer-adv`) provides all of the functionality (and more) of the Standard Model.

.. endif::

.. if:: devo8

**Advanced GUI**:

.. image:: images/devo8/ch_model/model_menu_conn.*
   :align: center
   :width: 80%

**Standard GUI**:

.. image:: images/devo8/ch_model/model_menu_std.png
   :align: center
   :width: 45%

.. endif::
.. if:: devo10

.. cssclass:: noborder

.. list-table::
   :widths: 5 45 45 5

   * -
     - **Advanced Model Menu**
     - **Standard Model Menu**
     -
   * -
     - .. image:: images/devo10/ch_model/model_menu_adv.png
          :width: 100%
     - .. image:: images/devo10/ch_model/model_menu_std.png
          :width: 100%
     -
.. endif::

.. cssclass:: bold-italic

Note: The Advanced Mixer GUI is the default setting for all new models.

.. _model-setup:

Model setup (Std & Adv GUI)
---------------------------

.. image:: images/|target|/ch_model/model_setup.png
   :align: center

The model page provides various model configuration options.

.. image:: images/|target|/ch_model/model_load.png
   :align: center

**File**: The File spin-box allows loading a new model, copying the existing model to a new location, resetting the current model to the default (all configuration is lost), and loading templates (see :ref:`predefined-model-templates`).  Note that changing models may result in a safety message being displayed (see :ref:`safety-system`).

.. if:: devo10

.. cssclass:: noborder

.. list-table::
   :widths: 5 45 45 5

   * -
     - .. image:: images/devo10/ch_model/model_copy.png
     - .. image:: images/devo10/ch_model/model_reset.png
     -

.. endif::

.. image:: images/|target|/ch_model/switch_mode.png
   :align: center

.. container::

   **Mixer GUI**: Defines which graphical user interface (GUI) to use for
   this model.  The ‘Advanced’ GUI is the default for Deviation.  The
   ‘Standard’ GUI is only available for Helicopter models and more closely
   resembles the stock GUI.

   Standard mixer gui is designed for collective pitch helicopters
   with a flybar. It includes features spefic to those that aren't needed
   on other aircraft, and may be missing features needed to properly
   control other aircraft. A flybarless collective pitch helicopter might
   benefit from some of the features of the standard GUI, it doesn't need
   them and may need those missing features. **You are strongly
   encouraged to use advanced mixer for all aircraft but collective pitch
   helicopters.**

   .. cssclass:: bold-italic

   Note: If you switch from advanced mixer to standard mixer all data
   may be lost.  Your data will be preserved if you switch from
   standard mixer to advanced mixer.

.. image:: images/|target|/ch_model/model_name.png
   :align: center

**Model Name**: Set the model’s name. Use the left, right, up, and down buttons then ENT to select each character.

.. image:: images/|target|/ch_model/model_icon.png
   :align: center

**Icon**: Choose the model’s icon.   Additional model icons can be installed (see :ref:`usb-file-system`).

.. image:: images/|target|/ch_model/helicopter_opts.png
   :align: center

.. container:: 

   **Model Type**: Set the model-type available options are Heli,
   Plane and Multi. Helicopter models have an additional configuration
   page that can be accessed by clicking the Model type. The options
   for SwashType are identical to the ones in
   :ref:`swash-configuration`.

   If you switch from model type Helicopter this will change the Mixer GUI to Advanced automatically because the Standard GUI only supports helicopters.

**Transmitter Power**: Specify the radio output power (when applicable). Available options are 100µW, 300µW, 1mW, 3mW, 10mW, 30mW, 100mW, 150mW. 

.. if:: devo10

.. cssclass:: bold-italic

Note: A stock Devo7e transmits with 7mW. Due to software configuration
150mW will always be displayed.

.. endif::

**PPM In**: Allows input from the DSC port primarily to control
external hardware such as camera motors from a 'head
tracker'. Secondarily it may be used to enable the transmitter to act
as a Master in a buddy-box setup. Available options are Channel,
Stick and Extend.

The Stick and Channel modes are used for buddy-box setup and documentation can be found in chapter :ref:`setting-up-a-buddy-box`.  The Extend mode is used for FPV or external input setup and documentation can be found in chapter :ref:`setting-up-fpv`. 

**Protocol**: Set the type of receiver being used.  Note that some
protocols have additional options that can be accessed by pressing
the Protocol spin-box when it is active.  See section
:ref:`protocols` for more on specific protocols.  Note that a
protocol change will disable any currently active protocol and will
affect any active model.  To enable the newly chosen protocol, use
the Bind/Re-Init button described below.

.. image:: images/|target|/ch_model/binding.png
   :align: center

**Bind/Re-Init**:  Depending on the protocol and Fixed-ID setting, the transmitter may bind with the model on start-up, or may need to be manually bound once.  See :ref:`protocols` for more on specific protocols.  If the protocol does not support binding, the button will show ‘Re-Init’, which can be used to switch protocols without power-cycling the transmitter. 
   
.. image:: images/|target|/ch_model/fixed_id.png
   :align: center

**Fixed ID**:  The Fixed ID sets a unique code to ensure that the transmitter will only bind to a specific model.  This is useful to ensure that the transmitter is not accidentally bound to the wrong model. 

**# Channels**: Sets the number of channels to transmit (the maximum number of channels is dependent on the selected protocol).

.. _predefined-model-templates:

Predefined Model Templates
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/templates.png
   :align: center

.. container::

   The Deviation firmware supports user-customizable predefined templates.  By Selecting ‘Template...’ within the File spin-box from the Model page. 

   Additional templates can be added via USB to the ‘\\template’ directory. A template does not completely replace your existing model, but instead only a portion of it.  The currently supported templates will replace the mixer and trim definitions, but will not affect the display layout.

.. _mixer-adv:

Mixer (Adv GUI)
---------------

.. if:: devo8

.. image:: images/devo8/ch_model/mixer_main.*
   :align: center
   :width: 80%

.. endif::
.. if:: devo10
 
.. image:: images/devo10/ch_model/mixer_main.png
   :align: center

.. endif::

.. container::

   The 'Advanced' GUI unleashes the full capabilities of the Deviation firmware, however it is unlike any commercial transmitter setup. Deviation also provides a more traditional setup interface for those who prefer it (see :ref:`standard-gui`). With the Advanced GUI, each output channel is composed of a series of one or more mixers each of which consists of a single input, an activation switch, and a function/curve that modifies the mixer output. This is a very powerful capability, but it will require learning a completely different method for setting up a model. To aid in quick setup, there are a few predefined configurations available (see :ref:`predefined-model-templates`), but to learn to modify and configure a model, read through this entire section carefully.

   The Mixer page controls how inputs (sticks/switches) are assigned to output channels.  The mixer page is accessed from the main menu by selecting the model icon..
 
   The number of channels available is dependent on the number of channels selected in section :ref:`model-setup`. Additionally there are 10 Virtual channels that can be used as an intermediate step for complex setups. 

Channel Reorder
~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/reorder_channels.png
   :align: center

The Channel reorder page allows moving mixer definitions between channels as well as duplicating channel configurations.  Note that the values displayed are the initial channel assignments.  Whenever the page is loaded, the channels will be sequentially ordered representing the current state.

.. _channel-config:

Channel configuration
~~~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/channel_limits.png
   :align: center

.. container::

   The Channel configuration provides the ability to configure the final channel outputs.  Capabilities such as channel reverse and fail-safe values are applied here.  Also available are controls for end-points, scaling, sub-trim, and a safety switch (which could be used to ensure that a motor cannot spin-up while working on a model)

   Changes to this page will immediately effect the channel output.  Pressing '**Cancel**' will restore the shown values to their last saved state.

   **Reverse**: Reverse the direction of servo rotation

   **Fail-safe**:  Specifies a value that the receiver should use when it loses signal from the transmitter. The range is between -125 and +125 or None. Not all receivers support this capability.

   **Safety**: Specifies a switch that will override all mixers and force the channel output to ‘Safe Val’ when flipped.

   **Safe Val**: If a safety switch is chosen the Safe Val can also be specified. The acceptable range of Safe Val is any value between -150 and 150.

   **Min Limit/Max Limit**: These values define the minimum and maximum values that the transmitter will ever send to the receiver (after all scaling, trims and mixer are applied).  If a calculated value is outside the min/max range, it will be clipped to either the min or max value as appropriate. Default is -150 for Min Limit and +150 for Max Limit. Maximum setting is -250 to 0 for Min Limit and 0 to 250 for Max Limit.

   **Scale-/Scale+**: These values define a final scalar to adjust the servo throw. Allowed entries are between 1 and 250. When you alternate Scale+  Scale- will be changed in the same way. If Scale- has been set to a different value than Scale+ both data will act separately until you set them to the same value again.

   **Subtrim**: Adjust servo zero position. The available range is between -50.0 and +50.0 in 0.1 increments.

   **Speed**: Adjust maximum servo speed.  Zero is disabled (fastest), Range is between 1 (slowest) and 250 (fastest). Servo speed is defined as number of degrees per 100msec (assuming a min/max throw of 120degrees).

     Example: A value of 60 will give a speed of 60degrees per 100msec which is equivalent to center-to max in 100msec. Most servos are rated at ~60degrees/0.1sec, so a speed > 60 will have no affect on most servos. A value of 30 should be approx twice as slow as a typical servo.

Virtual channel configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/channel_name.png
   :align: center

If you press ENT on a virtual channel a keyboard screen is shown where
you may edit the default name. You can use L/R/UP/DN buttons followed
by 'ENT' to select.
.. if:: devo8
Or just touch each character.
.. endif::

Simple Mix Type
~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/simple_template.png
   :align: center

.. container::

   The Simple mix type is the simplest manner of defining a channel.
   It allows defining a primary-input (stick, switch, or other
   channel), and applying a curve or function to that input.  The
   result can also be scaled or have an alternate zero-offset. You
   cannot use a toggle or switch to activate or deactivate this setup.

   A ‘Long-ENT’ press will update the current mixer settings, making it possible to test them on the transmitter.

   **Src**: The input source controlling this mixer.

   **Curve**: The function applied to the input to generate the output.  See section :ref:`available-curves` for more info.  Depending on curve-type, pressing curve may display the curve editor (see :ref:`curve-editing`).

   **Scale**: A multiplicative scalar that is applied after the Curve to control the output range.

   **Offset**: An additive offset that is applied after the scaling.

Expo & Dual-Rate Mix Type
~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/expo_dr.png
   :align: center

.. container::
   The Expo/Dual-Rate mix type is a more sophisticated template
   designed to allow use of toggle or 3-way switches to manipulate an
   input.  The primary-input (stick, switch, or other channel), can
   have a different curve/function and scaling for each toggle-switch
   position.

   Selecting a value for Switch1 or Switch2 will activate the corresponding section.  Each section can either have a 'linked' curve (curve is the same as the 'High-Rate' curve) in which case only the scalar can be modified, or alternatively can have an independent curve definition.  Pressing the 'Mid-Rate' or 'Low-Rate' button for a given switch will toggle between linked and independent curves.

   A ‘Long-ENT’ press will update the current mixer settings, making it possible to test them on the transmitter.

   **Src**: The input source controlling this mixer.

   **Curve**: The function applied to the input to generate the output.  See section :ref:`available-curves` for more info.  Depending on curve-type, pressing curve may display the curve editor (see :ref:`curve-editing`).

   **Switch1** or **Switch2**: Specify a switch to enable Medium or Low rates.

   **Scale**: A multiplicative scalar that is applied after the Curve to control the output range.

Complex Mix Type
~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/complex.png
   :align: center

.. container::

   The Complex mix type unlocks the full power of the mixer system.
   For a given channel, any number of mixers can be applied to affect
   the final result.  Each mixer is applied based on whether the
   specified switch is active, and can either replace, add to, or
   multiply to the previous mixers for this channel.  Using this
   system it should be possible to define an output channel as a
   combination of any number of inputs.

   A ‘Long-ENT’ press will update the current mixer settings, making it possible to test them on the transmitter.

   The Complex Mixer page has the following options:

   **Mixers**: Specify the number of mixers for this channel. If you increase the number a new mixer will be added after the last existing page.

   **Page**: Specify the current mixer page being edited.  Pressing the spin-box will allow reordering the pages of the current channel.

   **Switch**: Specify an optional switch which determines whether the current mixer is active.

   **Mux**: Defines how the current mixer is applied to the previously defined mixers for this channel.  Options are:

   * **Replace**: If this mixer is active, all previous mixers are ignored.
   * **Add**: Add the value of this mixer to the previous mixers.
   * **Mult**: Multiply the value of this mixer with the previous
     mixers. Note that the values are percentages, so multiplying by
     50 actually multiplies by .5.
   * **Max**: The output will be the greater of the current mixer vs the previous mixers.
   * **Min**: The output will be the lesser of the current mixer vs the previous mixers.
   * **Delay**: Delay the output of this mixer when used with a fixed curve. Scale of 100 represents 5 seconds delay. Can be varied by using scale or offset. 

   **Src**: The input source controlling this mixer.

   **Curve**: The function applied to the input to generate the output.  See section :ref:`available-curves` for more info.  Depending on curve-type, pressing curve may display the curve editor (see :ref:`curve-editing`).

   **Scale**: A multiplicative scalar that is applied after the Curve to control the output range.

   Note that while the scale value is limited to 100%, the mixer may provide a value larger than 100% if an offset is set or if the trim value is non-zero.

   **Offset**: an additive offset that is applied after the scaling.

   **Trim**: Selects whether or not any trims for the selected source are applied to this mixer.

\ 
A given mixer can be considered to have the general form:

     M(x) = if(*Switch*) { *Src* * *Curve* * *Scale* + *Offset*} else {0} + *Trim*

The combination of mixers for a given output channel is defined by the Mux type:

  For a ‘Replace’ mux:

     Cx = if(\ |Sn|\ ) {\ |Mn|\ } else if (\ |Sn-1|\ ) {\ |Mn-1|\ } … else if (\ |S0|\ ) {\ |M0|\ }

  For a ‘Multiply’ mux:

     Cx = if(\ |Sn|\ ) {\ |Mn|\ } else {1} * if (\ |Sn-1|\ ) {\ |Mn-1|\ } else {1} * … * if (\ |S0|\ ) {\ |M0|\ } else {1}

  For an ‘Add’ mux:

     Cx = if(\ |Sn|\ ) {\ |Mn|\ } else {0} + if (\ |Sn-1|\ ) {\ |Mn-1|\ } else {0} + … + if (\ |S0|\ ) {\ |M0|\ } else {0}

  For a ‘Max’ mux:

     Cx = MAX(if(\ |Sn|\ ) {\ |Mn|\ } else {0}, if (\ |Sn-1|\ ) {\ |Mn-1|\ } else {0},  …, if (\ |S0|\ ) {\ |M0|\ } else {0})

  For a ‘Min’ mux:

     Cx = MIN(if(\ |Sn|\ ) {\ |Mn|\ } else {0}, if (\ |Sn-1|\ ) {\ |Mn-1|\ } else {0},  …, if (\ |S0|\ ) {\ |M0|\ } else {0})

Cyclic
~~~~~~

.. if:: devo10

.. image:: images/devo10/ch_model/cyclic.png
   :align: center

.. endif::
**Cyclic1, Cyclic2, Cyclic3**: The 3 outputs of the helicopter swash-plate mix. These will represent the 3 servos connected to the helicopter swash-plate (see :ref:`swash-configuration`).

Reordering Mixers
~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/reorder_mixers.png
   :align: center

.. container::
   Since the ordering of mixers is important to the output, it is possible to reorder and/or copy mixers in order to facilitate building complex rules.  This page is accessed by pressing ENT on the ‘Page’ spin-box on the complex mixer page.

   Select the respective mixer and use the up/down buttons to move the order of the selected mixer.  Note that the mixer name represents its position when the reorder dialog was opened.  If the dialog is closed and reopened, all mixers will be shown as numbered sequentially.

   The reorder page can add new mixers or delete existing ones using the ‘+’ and ‘-’ buttons respectively.  A mixer can also be copied to an existing mixer (overwriting it in the process) by using the ‘Copy To’ functionality.

.. _available-curves:

Available Curves
~~~~~~~~~~~~~~~~

The following curve functions are supported:

* **1-to-1**: Output is equal to the input (not editable).
* **Fixed**: Output is constant regardless of input (offset editable).
* **Min/Max**: Output is -100 if input is less than the specified value and 100 otherwise.
* **Zero/Max**: Output is 0 if input is less than the specified value and 100 otherwise.
* **>0**: Output matches input when greater than the specified value, and 0 otherwise.
* **<0**: Output matches the input when less than the specified value, and0 otherwise.
* **ABSVAL**: Output is the absolute-value of the input (editing the specified value will alter how the absolute-value is applied) 
* **EXPO**: Apply exponential curve to the input for non-linear response (editable see :ref:`curve-editing`).
* **Deadband**: Output will not respond to input values near zero (editable see :ref:`curve-editing`).
* **Multi-point**: Curve is based on 3, 5, 7, 9, 11 or 13 user-defined
  points (editable see :ref:`curve-editing`).

The default value for any of the offsets in above mentioned curves is 0 (zero). If you change the curve for one input the offset will be transferred to the new curve if possible.

.. _curve-editing:

Curve Editing
~~~~~~~~~~~~~

.. if:: devo10
The Curve Editor is accessed by selecting the curve spin-box when it is selectable.  The 1-1 and Fixed curve types may not be edited, and the curve-box will not be selectable if one of these curves is currently active.
.. endif::

.. if:: devo8
The Curve Editor is accessed by pressing a graph or by pressing or selecting the curve spin-box when it is selectable.  The 1-1 and Fixed curve types may not be edited, and the curve-box will not be selectable if one of these curves is currently active.
.. endif::

The Curve editor page will be different depending on which curve is selected.  It is not possible to change the curve type from the curve editor (except when a multi-point curve is selected).  Values can be set using the spin-box or by touching the graph.

.. image:: images/|target|/ch_model/curve_minmax.png
   :align: center

For the Min/Max, Zero/Max, >0, <0, and ABSVAL, the controls allow setting the transition point along the x-axis.  A value of ‘0’ will be symmetric around the y-axis, positive or negative values will move the center point accordingly

.. image:: images/|target|/ch_model/curve_expo.png
   :align: center

For the Expo curve, the controls allow independently configuring the shape of the curve for values greater-than or less-than zero.

.. image:: images/|target|/ch_model/curve_deadband.png
   :align: center

For the Deadband curve, the controls allow independently configuring the deadband width for values greater-than or less-than zero.

.. image:: images/|target|/ch_model/curve_multipoint.png
   :align: center

For the Multi-point curves, each point can be individually set.  Points are set by choosing the point number and then choosing a value. The minimum number of points allowable is 3 the maximum number of points is 13.  Enabling 'Smooth' will apply a smoothing function rather than connecting points via straight lines.

.. _timers:

Timers (Std & Adv GUI)
----------------------

.. if:: devo8
 
.. image:: images/devo8/ch_model/timers.png
   :align: center
   :width: 80%

.. endif::
.. if:: devo10

.. image:: images/devo10/ch_model/timers.png
   :align: center

.. endif::

.. container::

   The timer page defines up to 4 available timers.  Timers can count either up or down, and can be enabled either manually from the main screen or by an input trigger (stick or switch).


   Available timers are stopwatch, countdown, stopwatch-proportional, countdown-proportional, and permanent.


   Timers can also be optionally configured to be reset via an alternate switch (only when using the Advanced GUI).


   Both proportional timers need an input between 0 and 100 to act correctly. If you use these timer for throttle a virtual mixer must be used as the input to scale -100 to 100 values into 0 to 100.

.. image:: images/|target|/ch_model/permanent_timer.png
   :align: center

The ‘permanent’ timers are similar to an odometer and have their values saved in the model.ini file. They will maintain their previous value when powering up the transmitter. You can set the timer by using the 'Set to' button and reset by pressing the 'Reset' button.


.. _telemetry-config:

Telemetry config (Std & Adv GUI)
--------------------------------


.. image:: images/|target|/ch_model/telemetry_config.png
   :align: center

.. container::

   The telemetry configuration page allows specifying alarms when specific telemetry events occur.

   * **Telemetry**: Specify the telemetry input to use for alarm
     control.  The set of values available will depend on the protocol.
   * **Equality**: Can be '>' or '<=' indicating whether a value above or below the target causes an alarm. Pushing the ENT button will play the alarm sound once.
   * **Target**: The target value for the alarm. Additionaly, by pushing the ENT button you can cycle through a time delay (between 0 and 9 seconds) for which the target value has to be continuously reached before triggering the alarm. 

.. _trims-and-virtual-inputs:

Trims and Virtual Inputs (Std & Adv GUI)
----------------------------------------

.. image:: images/|target|/ch_model/trims.png
   :align: center

.. container::

   The trim page allows assigning the trim buttons and trim step, as well as configuring buttons to work as virtual inputs (see :ref:`trim-as-virtual-switch`). It is accessed from the main menu via 'Model menu' followed by 'Trims'.

   If the ‘Input’ field is set to an input stick, then the trim can be
   applied as part of the mixer, and will operate as a typical trim
   control.  If the ‘Input’ field is set as a channel or
   virtual-channel output, the value is applied directly to the
   channel output.  In this case, the selected ‘Trim +’ and ‘Trim -’
   buttons can operate as a virtual stick to control an output
   channel.

.. image:: images/|target|/ch_model/trims2.png
   :align: center

.. container::

   The trim-step defines how sensitive the trims are to input.  The maximum number of trim steps is +/-100.  So a step size of 0.1 will allow a full +/- 10% of trim adjustment on the servo.

   The trim-step can be changed on the main screen. If you have to change the source also please use the dialog accessed by pressing the respective 'Input' button. Here you may also add a switch to the trim. If a switch is added to the trim, then it will have different trim values in each switch position.

.. _datalog:

Datalog (Std & Adv GUI)
-----------------------

.. if:: devo10
.. cssclass:: bold-italic

Note: This feature is not available for Devo7e.

.. endif::

The Datalog feature allows storing a history of input or output positions as well as telemetry info over a period of time. This can be used to examine and replay a flight as well as to visualize telemetry information at a later time. Logs are persistent and Deviation will continue writing to the end of the previous log by default.

.. image:: images/|target|/ch_model/datalog.png
   :align: center

.. container::

   * **# bytes left**: Indicates how many bytes can be written to the log before it is full.
   * **Enable**: Input which enables logging.
   * **Reset**: Clear the current log.
   * **Rate**: How often to write current info to the log file.
   * **Select**: Quickly set or reset which items are logged.
   * **Controls**: Following 'Select' are a list of all controls which may be logged. They include timers, inputs, outputs, and virtual channels, and Telemetry. The more items logged the faster the log will fill up.

**Logging more information**
By default, the log can only store 16kB of data. You can increase the amount of data to be stored by changing the datalog.bin file on the transmitter to a larger size. Deviation cannot increase the size of this file, so its size indicates the maximum data that can be stored.

**Note: This is a feature for advanced users only**. There is currently no software provided to analyze the logs, and they cannot be visualized from within the transmitter. Please check the downloads section on www.deviationtx.com for conversion tools.

.. _main-page-config:

Main page config (Std & Adv GUI)
--------------------------------

.. if:: devo8

.. image:: images/devo8/ch_model/mainpage_layout.png
   :align: center
   :width: 45%

.. endif::
.. if:: devo10

.. image:: images/devo10/ch_model/mainpage_layout.png
   :align: center

.. endif::

.. container::

   The main page config page is used to configure the main-page display.  This page allows definition of which elements are shown on the main page.


   The following types of objects can be displayed:


   * **Box**: Display a numeric value.  Values can be timers, channel values, stick inputs, etc.  There are two types of boxes: big and small.  The only difference is the size of the box and the text within it.
   * **Trimbar**: Display a trim value.  These generally are controlled by the trim switch and indicate what the current trim position is.  There are two types of trims.  V-Trims show a vertical bar, and H-Trims show a horizontal bar. After inserting all trims do have numbers only.
   * **Model (Icon)**: Display the icon related to the selected model.
   * **Battery**: Display the battery voltage.
   * **TxPower**: Displays the actual transmitter rating.
   * **Bargraph**: Displays a vertical bar.  The value of the bar is a
     channel output.
   * **Toggle**: Show an icon indicating the state of a toggle switch.  There can be 1, 2, or 3 icons defined for a given toggle indicating different states depending on the switch position.  Two-state switches can have up to 2 icons.  Three-state switches can have up to 3 icons. 
   * **(Quick) Menus**: Quick menus define quick-access pages that can be reached via a long UP/DN press.

.. _configuring-object-position:

Configuring object position
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. if:: devo8

Each of the visual objects can be selected by pressing on them, or with the UP/DN buttons followed by ENT.  Once selected, the UP/DN/L/R buttons will move the selected object on the screen.  Alternatively, the X and Y spin-boxes which appear in move mode can also be used to move the selected object.  Press EXT once to exit move mode.

.. endif::
.. if:: devo10

.. cssclass:: bold-italic

Note: This feature is not available for Devo7e.

.. image:: images/devo10/ch_model/layout_position.png
   :align: center

Pressing and holding the ENT button from the model configuration page will switch to the object position screen.  Each of the visual objects can be selected using the UP/DN buttons.  Pressing ENT again will allow moving the placement of the selected object.  The UP/DN/L/R buttons will move the selected object on the screen.  Press EXT once to exit move mode, and again to go back to the main page config menu.

.. endif::

Creating Objects
~~~~~~~~~~~~~~~~

.. if:: devo8

.. image:: images/devo8/ch_model/mainpage_createobj.png
   :align: center

Select the '+' icon to open the add-item dialog.  Then select the object type from the spin-box on the left, then press ‘Add’ to create the object.  This will add the specified object type to the center of the screen.  You can now place and configure the new object.

.. endif::
.. if:: devo10

.. cssclass:: bold-italic

Note: This feature is not available for Devo7e. 

Select the object type from the spin-box on the left, then press ‘**Add**’ to create the object.  This will add the relevant object type to the relevant section in the menu with a type of ‘None’ (where applicable).  Then move the cursor to the newly created object and configure as desired.

.. endif::

Loading Objects
~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/mainpage_load_layout.png
   :align: center

.. container::

.. if:: devo8
   After selecting the '+' icon to open the add-item dialog, you may 'Load' alternate templates, to change the main page layout.
.. endif::

.. if:: devo10
   You can 'Load' alternate templates, to change the main page layout.
.. endif::

   If you select 'Default' the layout will be set to the standard layout as shown in section :ref:`main-page`.

   Selecting 'Empty' will clear all objects. You may start from scratch.

   If you want to use a layout from another model select the model whose layout you wish to use. The object positions (see :ref:`configuring-object-position`) will be transferred when selecting from an existing template or model. Templates based on existing models have an (M) designation within the file list.

   Additionally these templates can be created in the emulator or downloaded from the forums or even done by manual edit of the modelxx.ini file.

Configuring Objects
~~~~~~~~~~~~~~~~~~~

* **Box**: Select timer, telemetry, channel, or input from scroll-box 
* **Trim**: Select trim channel from scroll-box
* **Model**: Not configurable 
* **Battery**: Not configurable
* **TxPower**: Not configurable
* **Bargraph**: Select channel from scroll box
* **Toggle**: Select channel or input from scroll-box.  Press related ‘Toggle’ button to choose icon
* **Menu**: Choose page to display for each of 4 quick-page slots

.. if:: devo8

.. image:: images/devo8/ch_model/mainpage_edit.*
   :align: center
   :width: 80%

You can delete any object by configuring the object and pressing the ‘Delete’ button
.. endif::
.. if:: devo10

You can delete any object but a Menu page by selecting the  ‘Delete’
option and pressing the 'ENT' button.

.. endif::

Choosing toggle icons
~~~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/choose_toggle.png
   :align: center

Pressing the ‘Toggle’ button on a toggle object allows selecting the related icons. Channels, sticks, and 2-position sticks can have 2 icons.  3 position sticks (if any) can have 3 icons.  Each of the 2 (or 3) icon states can be set to empty, defining that no icon is shown for this state.  The Deviation firmware comes with several predefined icons to choose from.

.. _standard-gui:

Standard GUI Menu items
-----------------------

.. image:: images/|target|/ch_model/model_menu_std.png
   :align: center

.. container::

   The Standard GUI is an alternative interface from the Advanced GUI’.  Which interface is used is chosen by the ‘Mixer GUI’ setting in section :ref:`model-setup`.  The Standard GUI is only available for Helicopter-type models at this time.  The pages of the Standard GUI are as follows:

.. if:: devo8

.. list-table::
   :widths: 10 40 10 40

   * - .. image:: images/devo8/ch_model/icon_modelcfg.png
     - **Model Configuration**: :ref:`model-setup`
     - .. image:: images/devo8/ch_model/icon_trim.png
     - **Trim configuration**: :ref:`trims-and-virtual-inputs`
   * - .. image:: images/devo8/ch_model/icon_servo_reverse.png
     - **Servo reverse**: :ref:`servo-reverse`
     - .. image:: images/devo8/ch_model/icon_switch_assign.png
     - **Switch assignment**: :ref:`switch-assignment`
   * - .. image:: images/devo8/ch_model/icon_servo_trim.png
     - **Servo sub-trim**: :ref:`sub-trim-adjustment`
     - .. image:: images/devo8/ch_model/icon_throttle_hold.png
     - **Throttle-hold configuration**: :ref:`throttle-hold`
   * - .. image:: images/devo8/ch_model/icon_travel_adjust.png
     - **Servo travel-adjust**: :ref:`servo-travel-adjust`
     - .. image:: images/devo8/ch_model/icon_failsafe.png
     - **Fail-Safe configuration**: :ref:`fail-safe-configuration`
   * - .. image:: images/devo8/ch_model/icon_swash.png
     - **Swash Setup**: :ref:`swash-configuration`
     - .. image:: images/devo8/ch_model/icon_timer_config.png
     - **Timer configuration**: :ref:`timers`
   * - .. image:: images/devo8/ch_model/icon_dualrate.png
     - **Dual-rates setup**: :ref:`dual-rate-expo-setting`
     - .. image:: images/devo8/ch_model/icon_telemetry_config.png
     - **Telemetry configuration**: :ref:`telemetry-config`
   * - .. image:: images/devo8/ch_model/icon_throtte_curve.png
     - **Throttle curve setup**: :ref:`throttle-curve`
     - .. image:: images/devo8/ch_model/icon_datalog.png
     - **Datalog configuration**: :ref:`datalog`
   * - .. image:: images/devo8/ch_model/icon_pitch_curve.png
     - **Pitch curve setup**: :ref:`pitch-curve`
     - .. image:: images/devo8/ch_model/icon_mainpagecfg.png
     - **Main page configuration**: :ref:`main-page-config`
   * - .. image:: images/devo8/ch_model/icon_gyro.png
     - **Gyro-sense configuration**: :ref:`gyro-sensitivity`
     -
     -

.. endif::
.. if:: devo10
.. container::

   1. **Model setup**: Model configuration page (See section  :ref:`model-setup`)
   2. **Reverse**: Servo reverse
   3. **D/R & Exp**: Dual-rates setup
   4. **Subtrim**: Servo sub-trim
   5. **Travel adjust**: Servo travel-adjust
   6. **Throttle curves**: Throttle curve setup
   7. **Pitch curves**: Pitch curve setup
   8. **Throttle hold**: Throttle-hold configuration
   9. **Gyro sense**: Gyro-sense configuration
   10. **Swash**: Swash Setup
   11. **Fail safe**: Fail-Safe configuration
   12. **Switch assignment**: Assign switch controls
   13. **Timers**: Timer configuration (See section :ref:`timers`)
   14. **Telemetry config**: Configure telemetry alarms (See section :ref:`telemetry-config`)
   15. **Datalog**: Configure telemetry logging (See section :ref:`datalog`)
   16. **Main page config**: Configure main page display (See section :ref:`main-page-config`)

.. endif::

.. _servo-reverse:

Servo Reverse
~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/servo_reverse.png
   :align: center

The servo reverse page allows quickly setting each channel to work in either normal or reversed mode.  These settings are equivalent to the ‘Reverse’ setting on the Channel Configuration sub-page of the Mixer menu when using the Advanced GUI (see section :ref:`channel-config`)

.. _dual-rate-expo-setting:

Dual-Rate/Expo setting
~~~~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/dualrate.png
   :align: center

The dual-rate and expo page allows configuration of curves for the Aileron, Rudder, and Elevator channels.  Up-to 3 rates can be configured for each channel, and either a scaled-linear or exponential curve can be selected for each.  The number of settings depends on the switch assigned to the dual-rates function on the Switch Assignment page (see :ref:`switch-assignment`)

.. _sub-trim-adjustment:

Sub-trim Adjustment
~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/subtrim.png
   :align: center

The sub-trim adjust page allows setting the zero-point of the servos for each channel.  This is equivalent to the ‘Subtrim’ setting on the Channel Configuration sub-page of the Mixer menu when using the Advanced GUI (see :ref:`channel-config`). Acceptable values range from -50 to +50 in 0.1 increments.

.. _servo-travel-adjust:

Servo Travel Adjust
~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/travel_adjust.png
   :align: center

The servo-travel adjust page configures the maximum positive/negative travel of each servo.  This is equivalent to the ‘Scale+’ and ‘Scale-’ settings on the Channel Configuration sub-page of the Mixer menu when using the Advanced GUI (see :ref:`channel-config`). Acceptable values for Down are from -175 to -1 and Up values range from +1 to +175. The default values are -100 and +100 respectively.

.. _swash-configuration:

Swash Configuration
~~~~~~~~~~~~~~~~~~~

The Swash configuration page configures the swash type.  More information about swash-types can be found in section :ref:`swash-mixing`.  The settings on this page are equivalent to those on the model configuration page (see :ref:`model-setup`), and configuration for both pages is provided below.

.. if:: devo8
.. image:: images/|target|/ch_model/swashmix.*
   :align: center
   :width: 90%
.. endif::
.. if:: devo10
.. image:: images/|target|/ch_model/swashmix.*
   :align: center
   :width: 80%
.. endif::

The available SwashType values are:

* **None/1Servo**: Used For FBL.  Mixing occurs in receiver
* **120/3Servo 120**: 120-degree swash
* **120x/3Servo 120x**: 120 degrees swash (alternate config)
* **140/3Servo 140**: 140 degree swash
* **90/3Servo 90**: 90 degrees swash

The ELE Mix, AIL Mix, and PIT Mix are scaling factors applied to the input sticks before mixing is done.  These can be used to adjust for different linkage lengths or different servo throws.  The allowed range is -100 to 100 with a default of 60.  
Note that setting these values too large can result in too much servo throw and make the model unresponsive to stick control.

.. _throttle-curve:

Throttle Curve
~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/throttle_curve.png
   :align: center

The throttle curve page allows defining a piece-wise linear curve for the throttle channel.  Different curves can be selected for each flight-mode.  Each point value can be enabled to be interpolated from the points surrounding it.

.. _pitch-curve:

Pitch Curve
~~~~~~~~~~~

.. image:: images/|target|/ch_model/pitch_curve.png
   :align: center

The pitch curve allows defining a piece-wise linear curve for the collective/pitch channel.  Different curves can be selected for each flight-mode as well as for throttle-hold.  Each point value can be enabled to be interpolated from the points surrounding it.

.. _gyro-sensitivity:

Gyro Sensitivity
~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/gyro_sense.png
   :align: center

The gyro-sensitivity page enables configuring up-to 3 sensitivity values for the gyro as well as which channel to use for sending the gyro value. Acceptable values range from 0 to 100%.

.. _switch-assignment:

Switch Assignment
~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/switch_assign.png
   :align: center

The switch assignment page enables configuring which switches to use for each capability in the standard-GUI.  The same switch may be assigned to multiple capabilities.

.. _throttle-hold:

Throttle Hold
~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/throttle_hold.png
   :align: center

The throttle-hold page is used to enable/disable the throttle-hold capability.  Specifying ‘Hold position’ defines the throttle value when the Throttle-hold switch is set. Hold position can be set from -200 to 200.

.. _fail-safe-configuration:

Fail-Safe Configuration
~~~~~~~~~~~~~~~~~~~~~~~

.. image:: images/|target|/ch_model/failsafe.png
   :align: center

The fail-safe page is used to configure the fail-safe value for each channel (if the protocol supports this feature)

