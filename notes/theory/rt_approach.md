I suspect Task and Robot morphology is coupled (assumption, citation needed).

**Top-down vs bottom-up**

*Top-down*: Start with a complex robot trying to solve a complex task. Then, try to decompose the task into skills. This is very hard to make it sample efficient. Most likely need to use vector reward(apparently this is called Multi Obj RL) and pass back a vector of gradients too.
I need to come back to this at some point, coz the tree of [robot morp x task] is diverging exponentially.

*Bottom-up*: Start with simple robot and simple task, slowly build from there. 


**pos control vs torque control**

*contact-rich-torque-control* Robot arm ee force applied to the env is optimized for. Very important for good object manipulation. Will come back to this later.

*pos control* is easier to learn, but not as good for manipulation. Will start with this for now.

