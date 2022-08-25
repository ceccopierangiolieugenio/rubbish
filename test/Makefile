.PHONY: testPyodide build

.venv:
	python3 -m venv .venv
	. .venv/bin/activate ; \
	pip install -r ../docs/requirements.txt

testPyodide:
	python3 -m http.server --directory ./

build:
	rm -f TermTk.tgz demo.tgz tutorial.tgz
	find ../TermTk/  -name "*.py" | sort | xargs tar cvzf TermTk.tgz
	find ../tutorial -name "*.py" | sort | xargs tar cvzf tutorial.tgz
	find ../demo/paint.py ../demo/ttkode.py ../demo/demo.py ../demo/showcase/*.* | sort | xargs tar cvzf demo.tgz