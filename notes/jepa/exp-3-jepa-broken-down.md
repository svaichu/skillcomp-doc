I like the idea that JEPA tries to neglect pixel level or brightness or texture, etc.

Command: PDDL or FoL or Strips

Obs: Each modality seperate encoder.
State(joint pos, vel, emboidiment cfgs), Vision (wrist cam, head cam, 3rdPOV),..

$$\it{w_t} = \it{Encoder}(\it{obs_{modality_n,t}})$$

Action: Similar to latent-action method, hierachy of skills. But each skill is a encoder, 

<!-- latex math eqn -->
$$\it{z_t} = \it{Encoder_{Action_n}}(\it{w_t})$$

Then planning in the latent space.


Inference:
1. Encode all modalities obs into w_n,t
2. Command: trigger a higher order skill(args, w_n,t)
3. Inside that skill.
    - Encode input into z_t and z_goal
    - List available option(args)
    - Choose sequence of option(args) to reach z_goal.



Training:
1. Obs encoder
2. 0th skill
3. nth skill

Obs encoder:


0th skill: example, line , circular, etc
Online gymanisium env


nth skill:
Online gymanisium env with a flag or binary reward. 
Do jepa style learning for encoder.
Predictor function


Question:
1. In options, selecting crt behaviour is difficult. is it made simpler by using jepa?
