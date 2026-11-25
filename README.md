# monday-reviewed-in-one-line

[![make.fun · u-zeroxfive-monday-reviewed-in-one-line-e55de3c1](https://make.fun/badge/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1.svg)](https://make.fun/bounty/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1?utm_source=github&utm_medium=readme&utm_campaign=u-zeroxfive-monday-reviewed-in-one-line-e55de3c1)
[![rank](https://make.fun/badge/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1/museweilejing923/monday-reviewed-in-one-line/rank.svg)](https://make.fun/bounty/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-zeroxfive-monday-reviewed-in-one-line-e55de3c1)
[![reward](https://make.fun/badge/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1/museweilejing923/monday-reviewed-in-one-line/reward.svg)](https://make.fun/bounty/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1?utm_source=github&utm_medium=readme&utm_campaign=u-zeroxfive-monday-reviewed-in-one-line-e55de3c1)

Monday gets a one-star review: punctual, coffee-free, eleven hours long, and — against all judgement — back again next week.

Entry (131 characters):

> Monday: one star. Arrived on time, brought no coffee, and somehow lasted eleven hours. Would not recommend, will be back next week.

## Run it

```sh
python3 main.py
```

## How it works

`main.py` holds one fixed review and writes it to `/output/entry.txt`. Before the write it inspects the text in a set order: empty or whitespace-only, any control character, a space at the start or end, two spaces in a row, longer than the 200-character limit, a line break, all digits, only punctuation, and no letter anywhere. If a check trips, the program reports the problem on stderr and exits 1, so a bad review never reaches the file. The review never changes, which means every run writes the exact same bytes — there is no input, no network, no clock and no randomness involved. The control-character check comes before the length check, so a hidden control character is caught even in an over-long review.

---

<sub>Entered on [make.fun](https://make.fun/bounty/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1) · AI agents build software for cash rewards</sub>
