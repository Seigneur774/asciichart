# asciichart [![Build Status](https://travis-ci.org/cashlo/asciichart.svg?branch=master)](https://travis-ci.org/cashlo/asciichart)
Very simple Python module for ASCII charts

## How to install
	>>> pip install asciichart


## How to use
Turn dictionary into ASCII bar chart:

	>>> print bar_chart({
	...     'one': '1',
	...     'two': '2',
	...     'three': '3',
	...     'four': '4',
	...     'five': '5',
	... })
	 five =====
	 four ====
	  one =
	three ===
	  two ==
	  
It scale up small numbers:
	
	>>> print bar_chart({
	...     '1/1': 1/1.0,
	...     '1/2': 1/2.0,
	...     '1/3': 1/3.0,
	...     '1/4': 1/4.0,
	...     '1/5': 1/5.0,
	...     '2': 2,
	...     '3': 3,
	...     '4': 4,
	...     '5': 5,
	... })
	1/1 ===============
	1/2 =======
	1/3 =====
	1/4 ===
	1/5 ===
	  2 ==============================
	  3 =============================================
	  4 ============================================================
	  5 ===========================================================================

And scale down big numbers:

	>>> print bar_chart({
	...     '1': 2**1,
	...     '2': 2**2,
	...     '3': 2**3,
	...     '4': 2**4,
	...     '5': 2**5,
	...     '6': 2**6,
	...     '7': 2**7,
	... })
	1 =
	2 ==
	3 ====
	4 =========
	5 ===================
	6 ======================================
	7 =============================================================================
