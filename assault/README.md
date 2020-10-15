assault
A simple CLI load testing tool.

installtion
Install using 'pip': ... $ pip install assault ...

usage
The simpplest usage of 'assault' requires only a URL to test against and see requests synchronously (one at a time) . This is what is would look like: ... $ assault https://example.com .... Done! .... Results! ... Successfule requests 500 Slowest 0.010s Fastest 0.001s Average 0.003s Total Time 0.020s Requests Per Minute 48300 Requests Per Second 800

If we want to add concurency we'll use the '-c' option and we can use the '-r' option to specify how many requests that we's like to make:

$ assault -r 3000 -c 10 http://example.com


##

pip3.7 install --user pipenv
pipenv install --python python3.7 twine --dev
