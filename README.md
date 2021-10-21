# calculator_zmq_protobuff
A practice to implement calculator using **Remote Procedure Call (RPC)** using ZeroMQ and Protocol Buffers.

The main calculation is done by `calculator` that will parse string and return result.
`single_thread`,`multi_thread`,`load_balancer` are different implementation of communication type, which is mainly for getting familiar with ZeroMq (cppzmq).
`proto` defined the message used in communition. Protocol Buffers provides message serialization function. 

## Calculator
### Functionalities
- Calculator
  Given "1+2*(9-6)" will return 7
- Solver
  Given "1*2+ ? = 9" will return 7
### Aim
- Design pattern: interpreter
- Excetion handling if there is invalid input
- Future might rewrite using boost_spirit

## Communication
### Functionalities
- Single thread approach
- Multi thread approach
- Load balancer approach
### Aim
- Practice ZeroMQ from simple to complex 
- Check Message loss
- memory leaks

## Serialization
### Protocol Buffers
### Aim
- Reduce data copy
- get to know zeroCopy
