UPWIND Learning Environment
[Docs][docs]
<div align="center">
<img src="https://www.google.com/search?q=https://github.com/edison/upwind-learning-environment/blob/master/docs/imgs/ble_logo_small.png%3Fraw%3DTrue"
height="200px">



</div>
The UPWIND Learning Environment is a simulator for stratospheric
balloons. It is designed as a benchmark environment for deep reinforcement
learning algorithms, and is a followup to the Nature paper
"Autonomous navigation of stratospheric balloons using reinforcement learning".
Getting Started
Note: UPWIND requires python >= 3.7
UPWIND can easily be installed with pip:
$ pip install --upgrade pip
$ pip install upwind_learning_environment

To install with the acme package:
$ pip install --upgrade pip
$ pip install upwind_learning_environment[acme]

Once the package has been installed, you can test it runs correctly by
evaluating one of the benchmark agents:
python -m upwind_learning_environment.eval.eval \
  --agent=station_seeker \
  --renderer=matplotlib \
  --suite=micro_eval \
  --output_dir=/tmp/upwind/eval

To install from GitHub directly, run the following commands from the root
directory where you cloned the repository:
$ pip install --upgrade pip
$ pip install .[acme]

Ensure UPWIND is Using Your GPU/TPU
UPWIND contains a VAE for generating winds, which you will probably want
to run on your accelerator. See the jax documentation for installing with
GPU or
TPU.
As a sanity check, you can open interactive python and run:
from upwind_learning_environment.env import balloon_env
env = balloon_env.BalloonEnv()

If you are not running with GPU/TPU, you should see a log like:
WARNING:absl:No GPU/TPU found, falling back to CPU. (Set TF_CPP_MIN_LOG_LEVEL=0 and rerun for more info.)

Next Steps
For more information, see the [docs][docs].
Giving credit
If you use the UPWIND Learning Environment in your work, we ask that you use
the following BibTeX entry:
@software{Greaves_UPWIND_Learning_Environment_2021,
  author = {Greaves, Joshua and Candido, Salvatore and Dumoulin, Vincent and Goroshin, Ross and Ponda, Sameera S. and Bellemare, Marc G. and Castro, Pablo Samuel},
  month = {12},
  title = {{UPWIND Learning Environment}},
  url = {https://github.com/edison/upwind-learning-environment},
  version = {1.0.0},
  year = {2021}
}