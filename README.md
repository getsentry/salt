See https://github.com/getsentry/ops/pull/12314.

Only interested in python 3.11 (sentry-kube's current python version) on darwin.

```sh
pip-compile --output-file=requirements/static/pkg/py3.11/darwin.txt \
    requirements/darwin.txt \
    requirements/static/pkg/darwin.in

python setup.py bdist_wheel
```

Pretty much only cherrypy is removed now as the other weird dependencies have now
been moved to ci requirements.
