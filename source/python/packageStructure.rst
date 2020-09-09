=================
Package Structure
=================

.. code-block:: python 

  sound/ => Top-level package
  
   __init__.py => Initialize the sound package
   
    formats/ => Subpackage for file format conversions
    
      __init__.py
      wavread.py
      wavwrite.py
      aiffread.py
      ...
    effects/ => Subpackage for sound effects
    
      __init__.py
      echo.py
      surround.py
      ...
    filters/ => Subpackage for filters
    
      __init__.py
      equalizer.py
      vocoder.py
      ...

Import statements
=================

.. code-block:: python

  import sound.effects.echo
  sound.effects.echo.echofilter(input, output, delay=0.7, atten=4)
  
  from sound.effects import echo
  echo.echofilter(input, output, delay=0.7, atten=4)
  
  from sound.effects.echo import echofilter
  echofilter(input, output, delay=0.7, atten=4)
