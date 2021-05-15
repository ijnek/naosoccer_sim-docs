Installation
############

Create a workspace and clone the repository:

.. code-block:: console

   mkdir -p ~/naosoccer_ws/src
   cd ~/naosoccer_ws/
   git clone --recursive https://github.com/ijnek/naosoccer_sim.git src/naosoccer_sim


Install dependencies:

.. code-block:: console

   vcs import src < src/naosoccer_sim/dependencies.repos
   colcon build