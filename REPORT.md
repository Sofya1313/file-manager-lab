# Lab 1 Report — File Manager
Name: Поварова Софья
Group: ИД24-2
OS: Linux Mint 22 (VirtualBox)
Date: 19.02.25

## Install and run commands
cd ~/projects/file_manager_project
python3 -m venv .venv
source .venv/bin/activate
python main.py

## Test scenario (commands + outputs)
fm> mkd docs
OK: created folder 'docs'
fm> new docs/a.txt
OK: created file 'docs/a.txt'
fm> put docs/a.txt "hello world"
OK: wrote 11 chars to 'docs/a.txt'
fm> read docs/a.txt
hello world
fm> show
{'cwd': '/', 'dirs': ['docs'], 'files': []}
fm> in docs
OK: entered 'docs'
fm> where
/docs
fm> out
OK: moved up one level
fm> ren docs/a.txt docs/b.txt
OK: renamed 'docs/a.txt' -> 'docs/b.txt'
fm> dup docs/b.txt docs/copy.txt
OK: copied 'docs/b.txt' -> 'docs/copy.txt'
fm> move docs/copy.txt moved.txt
OK: moved 'docs/copy.txt' -> 'moved.txt'
fm> del moved.txt
OK: removed file 'moved.txt'
fm> in ..
ERROR: Forbidden: attempted to escape workspace via '..'
fm> quit
QUIT

## Security check
in ..
ERROR: Forbidden: attempted to escape workspace via '..'

## Conclusion
Всё работает. Программа запускается, все команды выполняются, песочница блокирует выход за пределы workspace. Было сложно разобраться с ошибками в коде, но всё исправила.

## Home task

