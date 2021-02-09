# Code Task: Our Ninja Developer
---
## General Rules

 We need to create a tournament where several developers compete in several positions. Right now, the positions that existed are BackEnd and Testing (QC) positions. We plan to add more positions in the future.

You have been contacted to create a program to calculate the Ninja Developer (ND) of the given competition results.

You will receive a set of files, each one containing the stats of one competition. Each file will start with a row indicating the position it refers to.

Each developer is assigned a unique nickname. Each file represents a single day. The ND is the developer with the most rating points.

A developer will receive 10 additional rating points if their team won the competition. Every competition must have a winning team.

The program responsible for generating the files has a bug, that can be reflected in the wrong file format. If one file is wrong, the whole set of files is considered to be wrong and the MVP won't be calculated.

---

## BackEnd

Each row will represent one developer stats, with the format:
```
developer name;nickname;number;team name;position;scored points;rebounds;assists
```
This table details the rating points each developer in a backend competition receives depending on his position:
E.g. a developer acting as senior with `10 scored points`, `5 rebounds` and `no assists` will be granted `25 rating points` `(10*2 + 5*1 + 0*3)`.
The winner team is the one with more scored points.

|             | Scored point | Rebound | Assist |
| ----------- | ------------ | ------- | ------ |
| Junior (J)  | 2            | 3       | 1      |
| Mid    (M)  | 2            | 2       | 2      |
| Senior (S)  | 2            | 1       | 3      |


#### BackEnd Example

```csv
  BACKEND
  developer 1;nick1;4;Team A;G;10;2;7
  developer 2;nick2;8;Team A;F;0;10;0
  developer 3;nick3;15;Team A;C;15;10;4
  developer 4;nick4;16;Team B;G;20;0;0
  developer 5;nick5;23;Team B;F;4;7;7
  developer 6;nick6;42;Team B;C;8;10;0
```

---

## Testing (QC)

Each row will represent one developer stats, with the format:
```
developer name;nickname;number;team name;position;goals made;goals received
```
This table details the rating points each developer in a testing competition receives depending on his position:

|                   | Initial rating points | Bug Found | Error Occurred |
| ----------------- | --------------------- | --------- | -------------- |
| Manual (M)        | 50                    | 5         | -2             |
| Automation (A)    | 20                    | 1         | -1             |

E.g. a developer acting as `Manual QC` with `1 Bug found` and `10 Errors Occurred` will be granted `35 rating points` `(50 + 1*5 - 10*2)`.
The winner team is the one with more scored points.



#### Handball Example:

```csv
  Testing
  developer 1;nick1;4;Team A;G;0;20
  developer 2;nick2;8;Team A;F;15;20
  developer 3;nick3;15;Team A;F;10;20
  developer 4;nick4;16;Team B;G;1;25
  developer 5;nick5;23;Team B;F;12;25
  developer 6;nick6;42;Team B;F;8;25
```

---

## What we look at

You have `4 days` to complete the task, you should use `PHP laravel or Symfony frameworks` or `NodeJs Express or Adonis frameworks`. It is not mandatory to read input from file system. It is acceptable to read from stdin, forms or any other source.

- We are interested in how you structure your code.
- The code should be open for extension closed for modification `we should be able to add new sport without changing the core calculator`.
- We are interested in seeing how efficient the algorithm you implement is.
- We are interested in seeing how you unit test your code.

---

## Nice to Have:

- Dockerize your solution.
- Struct database schema.

---

## Submit your challenge:

Follow these instructions to submit your challenge:

- Clone the Challenge Repository
- Create a dedicated branch
- Write your Code
- Commit your Changes
- Fork the Challenge Repository
- Issue a Pull Request

