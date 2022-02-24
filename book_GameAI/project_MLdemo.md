---
title: Unity ML demo
parent: GameAI
has_children: false
nav_order: 99
---

# Unity ML demo project

1) ML-Agents
2) place on a plane in AR
3) put in a VR card board scene
4) publish in WebGL
5) publish on GooglePlay

## setup
Unity 2019.3.12f1 or later 
android, IILCP, 64 bit

## part: ML-Agents
see https://github.com/Unity-Technologies/ml-agents/blob/release_2_verified/docs/Learning-Environment-Create-New.md

verificare di aver isntallato il pacchetto Python + ml-agents

- add ml-agents package
- floor
- cube -> target
- sphere -> RollerAgent, add RigidBody
- put everything under TrainingArea

- add script RollerAgent

using Unity.MLAgents;
using Unity.MLAgents.Sensors;
eredito Agent

cahceo rigidbody

public override void OnEpisodeBegin() { }
public override void CollectObservations(VectorSensor sensor) { }
public override void OnActionReceived(float[] vectorAction) { }

resetto OnOpisodeBegin

```
public override void OnEpisodeBegin()
{
    if (transform.localPosition.y < 0) {
        rBody.angularVelocity = Vector3.zero;
        rBody.velocity = Vector3.zero;
        transform.localPosition = new Vector3(0, 0.5f, 0);
    }
    Target.localPosition = new Vector3(Random.value * 8 - 4, 0.5f, Random.value * 8 - 4);
}
```


colelcte observarions:

```
sensor.AddObservation(Target.localPosition);
sensor.AddObservation(transform.localPosition);
sensor.AddObservation(rBody.velocity.x);
sensor.AddObservation(rBody.velocity.y);
```

add onCation CONTROL
```
Vector3 controlSignal = Vector3.zero;
controlSignal.x = vectorAction[0];
controlSignal.z = vectorAction[1];
rBody.AddForce(controlSignal * speed);
```

finishe REQARDS

```
            float distanceToTarget = Vector3.Distance(transform.localPosition, Target.localPosition);
            if (distanceToTarget < 1.4f) {
                SetReward(1.0f);
                EndEpisode();
            }

            if (transform.localPosition.y < 0) {
                EndEpisode();
            }
```

configure Behavuoir:
name: RollerBall
action space: 8 observe + 2 receinve
Decision Requester: ogni 10

creare un config/rollerball_config.yaml

```
RollerBall:
  trainer: ppo
  batch_size: 10
  beta: 5.0e-3
  buffer_size: 100
  epsilon: 0.2
  hidden_units: 128
  lambd: 0.95
  learning_rate: 3.0e-4
  learning_rate_schedule: linear
  max_steps: 5.0e4
  memory_size: 128
  normalize: false
  num_epoch: 3
  num_layers: 2
  time_horizon: 64
  sequence_length: 64
  summary_freq: 10000
  use_recurrent: false
  reward_signals:
    extrinsic:
      strength: 1.0
      gamma: 0.99
```

entrare in ml-agents enf: source ~/python-envs/mlagents-env/bin/activate

e quindi: 

mlagents-learn config/rollerball_config.yaml --run-id=RollerBall

se voglio vedere il board: tensorboard --logdir=summaries --port=6006


metto nn
