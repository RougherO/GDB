## Breakpoints
- `break <function/line>` -> set breakpoint at <function/line> in current file
- `break <file>:<function/line>` -> set breakpoint at <function/line> in <file>
- `commands <breakpointNumber> [list of commands with one command per line] end` -> executes \[list of commands\] when <breakpointNumber> is hit.
- `condition <breakpointNumber> [condition]` -> sets a condition on <breakpointNumber>. <breakpointNumber> is hit when \[condition\] is hit. If \[condition\] is empty sets the breakpoint to unconditional.
- `delete breakpoints` -> deletes all breakpoints
- `delete breakpoints <breakpointNumber>` -> delete <breakpointNumber> breakpoint
- `disable <breakpointNumber>` -> disables <breakpointNumber>
- `info breakpoint` -> list all breakpoints and show comprehensive info
- `ignore <breakpointNumber> <count>` -> set <breakpointNumber> to be ignored for <count> times
- `watch <expression>` -> create a watchpoint to watch variables if their value changes. <expression> needs to be defined in current frame.

## Data
- `set listsize <number>` -> changes listsize settings for `list` to display only <number> lines
- `set disassmbly-flavor <intel/att>` -> set the diassmebly style
- `show disassmbly-flavor` -> show current disassembly style

## Running
- `continue` -> run program till next interrupt(breakpoint, error etc.)
- `finish` -> execute current function frame stack until it returns
- `next` -> execute next LOC and execute any function calls if any at current line but not step into it.
- `step` -> execute one line of code. If the line to be executed is a function call, step into that function and start executing its code one line at a time

## Stack
- `backtrace/where/bt` -> print single backtrace of current frame(useful to find out where the program is currently at).
- `backtrace/where/bt -full` -> show entire backtrace of stack frames for current frame
- `backtrace/where/bt [COUNT]` -> shows <COUNT> frames outside/inside of current stack frame depending on whether <COUNT> is positive or negative.
- `frame` -> shows current frame (useful for checking your location in file)

## Status
- `info <function/line>` -> show asm instruction address of <line> in current file
- `info <file>:<funciton/line>` -> show asm instruction address of <line> in <file>

## Support
- `quit/exit/q` -> exit GDB
