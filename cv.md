# Samsonenko Dmitry

## Contacts

- **Email:** [samsondm97@gmail.com](mailto:samsondm97@gmail.com)
- **LinkedIn**: [Dmitry Samsonenko](https://www.linkedin.com/in/samsonenkodm/)
- **Discord**: [fridaysd](https://discordapp.com/users/326460068717658122)
- **GitHub**: [Friday-13](https://github.com/Friday-13)

## About Me

I'm a beginner Python developer. I started my career as a embedded developer and created software on C for different small devices and measurement systems, wrote Python scripts for analize measurement results. Now I still work in this sphere as a self-employed and I'm going to change it to web-development.

I'm looking for a job in backed-development and work on improving my skills in this area. But I also interested in frontend development and other related to web-developments skills and tools. So self-education is important part of my life.

I am responsible, I work well in a team and can organize my working time. I like master new skills and always try to find common language with any project members. The result of my work: new app or new app feature that works and does something usefull is a real pleasure for me.

## Skills

- Python
  - Django
  - NumPy
  - Matplotlib
- JavaScript
- HTML / CSS
- SQL
- C
  - STM32-programming
- LaTEX

## Work History

- **Self-employed** \
  **time period:** December 2020 - Present \
  **position:** _Microcontroller software developer_

- **Research Institute of Automation of Production Processes** \
  **time period:** August 2020 - December 2020; July 2021 - December 2021 \
  **position:** _Microcontroller software developer_

- **TB.Budget** \
  **time period:** July 2014 - August 2014 \
  **position:** _Technical writer_

## Code Examples

### Python

LeetCode: [19. Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)

```python
class Solution:
    def removeNthFromEnd(self, head: Optional[ListNode], n: int) -> Optional[ListNode]:
        end_node = head
        prev_node = head
        for _ in range(n):
            end_node = end_node.next

        if not end_node:
            return head.next

        while end_node.next:
            end_node = end_node.next
            prev_node = prev_node.next

        prev_node.next = prev_node.next.next
        return head
```

### JavaScript

Codewars: [RGB To Hex Conversion](https://www.codewars.com/kata/513e08acc600c94f01000001/train/javascript)

```javascript
function rgb(r, g, b) {
  const constrain = (color) => {
    if (color < 0) return 0;
    if (color > 255) return 255;
    return color;
  };

  const toHex = (color) => {
    let hex = constrain(color).toString(16).toUpperCase();
    if (hex.length < 2) hex = "0" + hex;
    return hex;
  };

  return toHex(r) + toHex(g) + toHex(b);
}
```

### C

Filter function for digital measurements processing

```c
/**
 * @brief Runing average by 2 points.
 * You can adjust the filtering sharpness through the corresponding
 * argument field RunningAverageCoeff.
 * The measurement frequency greatly influences on the results.
 *
 * @param Signal - link to the RuningAverFilterStruct struct
 */
void RuningAverFilterHandler(RuningAverFilterStruct *Signal)
{
    Signal->SampleFreqCount++;
    if (Signal->SampleFreqCount >= Signal->SampleFreq)
    {
        Signal->SampleFreqCount = 0;
        Signal->Out = (Signal->Value - Signal->Out) * Signal->RunAverCoef + Signal->Out;
    }
    Signal->Filtered = 1;
}
```

### Projects

- [Simple browser game (html/css/js)](https://rolling-scopes-school.github.io/friday-13-JSFEPRESCHOOL2023Q2/random-game/)
- [Project with base blog functionality based on Django](https://github.com/Friday-13/dartblog)
- [C-based filters lib](https://github.com/Friday-13/libfilters)

## Education

- **Master's degree** \
   **time period:** 2019-2021 \
   **place:** Bauman Moscow State Technical Uiversity \
   **department:** Robotics and сomplex automation \
   **speciality:** Mechanical engineering

- **Bachelor's degree** \
  **time period:** 2015-2019 \
   **place:** Bauman Moscow State Technical Uiversity \
   **department:** Radioelectronics and laser technologies \
   **speciality:** Nanoengineering

### Other Education

- **JavaScript/Front-end 2023Q4** \
  **place:** The Rolling Scopes School \
  **time-period:** November 2023 - Present

- **English** \
   **place:** Yandex Practicum \
   November 2022 - Present

- [**JS/FE Pre-School 2023Q2 (javascript)**](https://app.rs.school/certificate/6jjl240p) \
   **place:** The Rolling Scopes School \
   **time-period:** July 2023 - November 2023

- [**Database design**](https://stepik.org/cert/1988834?lang=en) \
   **place:** Stepik \
   **time-period:** March 2022 - July 2022
- [**Advanced SQL**](https://stepik.org/cert/1962732?lang=en) \
   **place:** Stepik \
   **time-period:** March 2022 - July 2022
- [**Base SQL**](https://stepik.org/cert/1523830?lang=en) \
   **place:** Stepik \
   **time-period:** March 2022 - July 2022

## Languages

- **Russian** - native speaker
- **English** - C1 ([EFSET-cetify (C2 level)](https://www.efset.org/cert/AHim43))
