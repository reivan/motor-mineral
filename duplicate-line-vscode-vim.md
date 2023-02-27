I want to go from this:

```js
import { Filters } from './Filters';
```

To this:

```js
import { Filters } from './Filters';
import { Table } from './Table';
```

How to do it in Visual Studio Code:

1. duplicate line (Shift + Option + Down on Mac)
2. put cursor on the word Filter
3. Ctlr+d to select the next occurance of the word Filter
4. type Table

How to do it in Vim:

1. duplicate line (`dd`)
2. put cursor on the word Filter
3. copy word Filter (`yiw`)
4. start typing replace command (`:s/`)
5. paste Filter from a register (`Ctrl+R "`)
6. type Table (`/Table`)
7. don't forget to make replace global (`/g`)
8. press Enter to run the command

Why vim requires more keystrokes to do the same action? What am I doing wrong?
