- [v1.1.0](#v1.1.0)
- [v1.0.0](#v1.0.0)

## v1.1.0 - To be released
* Daily file handler. The file handler rollover every 24 hours
* Rotating file handler. The file handler will rollover based on the size of the file
* MinGW compatibility
* Added a CMake option `QUILL_VERBOSE_MAKEFILE`. Building Quill as a master project now defaults to non verbose makefile output unless `-DQUILL_VERBOSE_MAKEFILE=ON` is passed to CMake.
* Flush policy improvement. Previously Quill backend worker thread would never `flush`. This made watching the live log of the application harder because the user has to wait for the operating system to flush or `quill::flush()` had to be called on the caller threads. This has now been fixed, when the backend thread worker has no more log messages to process it will automatically `flush`
## v1.0.0
Initial release