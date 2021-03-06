**Added:**

* <news item>

**Changed:**

* xonsh/environ.py: new rule: for "registered" environment variables (in ``DEFAULT_VARS`` or via ``env.register()``), 
  if default is set to ``DefaultNotGiven``, then variable has no default and raises ``KeyError`` if it is not 
  actually defined in environment.  Likewise, ``"var" in __xonsh__.env`` will return False.
* Changed defaults for ANSICON, TERM and VIRTUAL_ENV to ``DefaultNotGiven``, so code can rationally test whether
  the expected external program has defined these variables.  No need to do this for variables that xonsh
  itself defines.

**Deprecated:**

* <news item>

**Removed:**

* <news item>

**Fixed:**

* Fixed #3703 and #3739, recent code change made it impossible to tell whether a (registered) environment variable
  was missing from environment or present and set to its registered default value. The test for ANSICON was
  failing due to this.

**Security:**

* <news item>
