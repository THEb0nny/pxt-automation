# Automation [![Build Status](https://travis-ci.org/Microsoft/pxt-automation.svg?branch=master)](https://travis-ci.org/Microsoft/pxt-automation)

Various algorithm for Systems & Control operations for Microsoft MakeCode editors.

## How to use this library?

In your MakeCode editor, click on the gearwheel menu and click "Extensions", search for "automation"
and select this project.

## PID controller

A Proportional-Integral-Derivative control is a classic control structure in automation.
The user needs to define 3 gains (``Kp``, ``Ki``, ``Kd``) to tune the controller.

See Reference: [Feedback System, Karl Johan Astrom & Rickard M. Murry](https://press.princeton.edu/titles/8701.html)

```blocks
let v = 0;
automation.pid1.setGains(1, 0.01, 0.001);
for (let i = 0; i < 10; ++i) {
    v = automation.pid1.compute(0.1, 5);
}
```

## Behaviors

An example of Behavior-based robotics control system. 

## Moving Average Filter

```blocks
let r = 0;
for (let i = 0; i < 10; ++i) {
    r = automation.movingAverageFilter1.filter(Math.random());
}
```

## Supported targets

* for PXT/maker
* for PXT/adafruit
* for PXT/codal
* for PXT/ev3

## License

MIT

## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
