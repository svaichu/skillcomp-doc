Control Key (latent dim) -> i-skill (ee-pos, only zero order)-> ik (joint pos) -> pos control (actuation) -> env (reward)

what should be the loss func?
1. ee_pos error:
$$L = ||ee\_pos\_pred - ee\_pos\_target||^2$$
Not a good option, coz we are not learing dynamics model, we need control policy.

2. reward only update:
Reward is sparse. mostly zero and 1 only at goal.
MC strategy maybe efficient here.


Control Key:
1. what should be the latent dim of the control key?
Skill: gotoGoal(target_ee_pos: 7dim, obs_ee_pos: 7dim)
Can this be replaced by anything less than 14 dim or even less than 7 dim would be fantastic?

**Train gotoGoal() skill**
1. Send up gradients only at goal state.
2. Normalize ee_pos around workspace. And get reachable_target_normalized().
3. Start from 1dof arm.

inputs are: norm_target_ee_pos, norm_obs_ee_pos

intermediate output: z

output: norm_delta_ee_pos