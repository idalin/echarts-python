Echarts for Python
==================

An unofficial Echarts options generator with Python.

.. image:: https://img.shields.io/pypi/v/Echarts.svg
   :target: https://pypi.python.org/pypi/Echarts/
   :alt: Latest Version
.. image:: https://travis-ci.org/yufeiminds/echarts-python.svg?branch=develop
   :target: https://travis-ci.org/yufeiminds/echarts-python
   :alt: Travis CI Status
.. image:: https://codecov.io/github/yufeiminds/echarts-python/coverage.svg?branch=develop
   :target: https://codecov.io/github/yufeiminds/echarts-python?branch=master
   :alt: Codecov Status
.. image:: https://readthedocs.org/projects/echarts-python/badge/?version=latest
   :target: http://echarts-python.readthedocs.org/en/latest/?badge=latest
   :alt: Doc Status

-  Free software: MIT license
-  Documentation: https://echarts-python.readthedocs.com/en/
-  Online demo: https://yufeiminds.github.io/echarts-python/

Installation
------------

Installing **echarts-python** with pip ::

  $ pip install echarts-python

Current version for `Echarts 3.1.6 <http://echarts.baidu.com/option.html>`_

Basic Usage
-----------

.. code-block:: python

    from echarts import Echart, Legend, Bar

    chart = Echart('GDP', 'This is a fake chart')
    chart.use(Bar('China', [2, 3, 4, 5]))
    chart.use(Legend(['GDP']))
    chart.use(Axis('category', 'bottom', data=['Nov', 'Dec', 'Jan', 'Feb']))

The `chart.json` property will be

.. code-block:: javascript

    {
        "series": [
            {
                "type": "bar",
                "zlevel": 0,
                "data": [2, 3, 4, 5],
                "name": "China"
            }
        ],
        "legend": {
            "y": "top",
            "x": "center",
            "data": [
                "China"
            ],
            "orient": "horizontal"
        },
        "title": {
            "text": "GDP",
            "subtext": "This is a fake chart"
        },
        "xAxis": [],
        "yAxis": []
    }


Contribution
------------

This package authored by Hsiaoming Yang <me@lepture.com> in 2014.

If you have any question or want to improve this repository, welcome to create
an `issue <https://github.com/yufeiminds/echarts-python/issues>`__
or `pull requests <https://github.com/yufeiminds/echarts-python/pulls>`__ .

This repo is maintained by Yufei Li <yufeiminds@gmail.com> now,
you can also send a email to me.
