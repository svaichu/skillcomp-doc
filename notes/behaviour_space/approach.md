
Behaviour space:
a ndof arm, there exists a set of behaviours that live in behaviour space.

behav_x = Fourier_Shapes_Space_ndof(cfg)
traj = behav_x(delta)


Also: Observation encoder.
w_t = state_encoder(obs_state_t)

skill_a(w_t, w_goal)
    z_t = skill_a_encoder(w_t)
    z_init -> behav_planning -> z_goal
Look into IQE objective for training encoder.

behav_planning(z_init,z_goal)
- minimum activations
- warm-start
- bundle behavs: from other skills.
- bundle behavs: same skill across time using z


Trainings:
1. Obs_encoder
2. Fourier_Shape_Space
3. skill_a_encoder
4. behav_planning for that skill
