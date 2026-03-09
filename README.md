# QAS_entanglement
This repository contains is an implementation of the "General-purpose quantum architecture search based on deep reinforcement learning".
The base-line method referred "https://github.com/qdevpsi3/quantum-arch-search".
In this code, the version repository has been upgraded to: Cirq (v1.4.1), Stable-Baselines3 (v2.4.0), and Gymnasium (v1.0.0).
Furthermore, this program has re-implemented the fidelity calculation method, the influence of noise, and the applying method of the quantum gates.

The default settings can be used in 3-qubit system. For 4-qubit or more condition, please change the env_name in notebook from 'BasicThreeQubit-v0' to 'BasicNQubit-v0'(or noisy env), then changing qas_env,please change the observation space and _get_obs, using "entanglement_a" rather than "entanglement", then don't use target_con = self.target_concurrence() , current_con = self.current_concurrence() and con_difference = abs(current_con - target_con). Please enable s_tot_norm, s_a_norm, s_b_norm = self._get_renyi() and use the con_difference = abs(self.s_a_norm_tar - s_a_norm), and use fidelity = self.fidelity_measure(),then change the coefficient of reward function(if you want).
