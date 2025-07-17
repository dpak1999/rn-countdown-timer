# Note

![CodeRabbit Pull Request Reviews](https://img.shields.io/coderabbit/prs/github/dpak1999/rn-countdown-timer?utm_source=oss&utm_medium=github&utm_campaign=dpak1999%2Frn-countdown-timer&labelColor=171717&color=FF570A&link=https%3A%2F%2Fcoderabbit.ai&label=CodeRabbit+Reviews)

THIS IS A PACKAGE FROM https://www.npmjs.com/package/react-native-countdown-component . Because of bugs this does not work with RN v74+ and there are no maintainers, hence the package is a fork and fixed version. 

All credit go to original [author](https://github.com/talalmajali/).

## Installation

Run `npm install @dpak1999/rn-countdown-timer --save` OR `yarn add @dpak1999/rn-countdown-timer --save`

## Props

| Name           | Description                                                  | Type   |                                      Default Value                                      |
| :------------- | :----------------------------------------------------------- | :----- | :-------------------------------------------------------------------------------------: |
| id             | Counter id, to determine whether to reset the counter or not | string |                                          null                                           |
| style          | Override the component style                                 | object |                                           {}                                            |
| digitStyle     | Digit style                                                  | object | {backgroundColor: ![#FAB913](https://placehold.it/15/FAB913/000000?text=+) `'#FAB913'`} |
| digitTxtStyle  | Digit Text style                                             | object |       {color: ![#FAB913](https://placehold.it/15/000000/000000?text=+) `'#000'`}        |
| timeLabelStyle | Time Label style                                             | object |       {color: ![#FAB913](https://placehold.it/15/000000/000000?text=+) `'#000'`}        |
| separatorStyle | Separator style                                              | object |       {color: ![#FAB913](https://placehold.it/15/000000/000000?text=+) `'#000'`}        |
| size           | Size of the countdown component                              | number |                                           15                                            |
| until          | Number of seconds to countdown                               | number |                                            0                                            |
| onFinish       | What function should be invoked when the time is 0           | func   |                                          null                                           |
| onChange       | What function should be invoked when the timer is changing   | func   |                                          null                                           |
| onPress        | What function should be invoked when clicking on the timer   | func   |                                          null                                           |
| timeToShow     | What Digits to show                                          | array  |                                  ['D', 'H', 'M', 'S']                                   |
| timeLabels     | Text to show in time label                                   | object |                   {d: 'Days', h: 'Hours', m: 'Minutes', s: 'Seconds'}                   |
| showSeparator  | Should show separator                                        | bool   |                                          false                                          |
| running        | a boolean to pause and resume the component                  | bool   |                                          true                                           |

## Preview

![React Native Countdown](https://media.giphy.com/media/xT0xeLWYNSaLerFGko/giphy.gif "React Native Countdown")

## Code

```javascript
import CountDown from '@dpak1999/rn-countdown-timer';

render() {
    return (
      <CountDown
        until={10}
        onFinish={() => alert('finished')}
        onPress={() => alert('hello')}
        size={20}
      />
    )
}
```

## Custom Styling Example

![React Native Countdown](https://media.giphy.com/media/wIwc1dinsZhx6v2PxB/giphy.gif "React Native Countdown")

## Code

```javascript
import CountDown from '@dpak1999/rn-countdown-timer';

render() {
    return (
      <CountDown
        until={60 * 10 + 30}
        size={30}
        onFinish={() => alert('Finished')}
        digitStyle={{backgroundColor: '#FFF'}}
        digitTxtStyle={{color: '#1CC625'}}
        timeToShow={['M', 'S']}
        timeLabels={{m: 'MM', s: 'SS'}}
      />
    )
}
```

## Separator Example

![React Native Countdown](https://media.giphy.com/media/4H7qQF4UPwQKEc0Qpx/giphy.gif "React Native Countdown")

## Code

```javascript
import CountDown from '@dpak1999/rn-countdown-timer';

render() {
    return (
      <CountDown
        size={30}
        until={1000}
        onFinish={() => alert('Finished')}
        digitStyle={{backgroundColor: '#FFF', borderWidth: 2, borderColor: '#1CC625'}}
        digitTxtStyle={{color: '#1CC625'}}
        timeLabelStyle={{color: 'red', fontWeight: 'bold'}}
        separatorStyle={{color: '#1CC625'}}
        timeToShow={['H', 'M', 'S']}
        timeLabels={{m: null, s: null}}
        showSeparator
      />
    )
}
```
