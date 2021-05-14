Running the Button Simulator
############################

Because SimSpark does not provide a way to interact with the buttons on the NAO, a separate command
line program was developed to simulate button presses.

In a new terminal, run ``ros2 run nao_button_sim nao_button_sim``.

To simulate a button press, click on a key specified in the assigned keys list below.

.. code-block:: console

    ---------  Assigned Keys  ---------                                 
    G - Chest button
    C - Left Foot Bumper Left
    V - Left Foot Bumper Right
    B - Right Foot Bumper Left
    N - Right Foot Bumper Right

The program provides visual feedback for which buttons are being pressed. The word "Pressed" will show
in the corresponding column, as shown below:

.. code-block:: console


    ---------------------------------------  BUTTON PRESS STATUS  ---------------------------------------

    |     Chest (G)     | LFoot BumperL (C) | LFoot BumperR (V) | RFoot BumperL (B) | RFoot BumperR (N) |
    =====================================================================================================
    |      Pressed      |                   |                   |      Pressed      |                   |

.. tip::

    Multiple keys can be pressed concurrently