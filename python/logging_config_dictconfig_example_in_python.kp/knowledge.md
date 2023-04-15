---
title: Can you show me a full illustration of logging.config.dictconfig?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: A complete example of logging.config.dictConfig in Python can be found in the official Python documentation.
---

**Contents**

[TOC]

# Overview
`logging.config.dictConfig` is a method in the Python logging module that allows configuring logging using a dictionary-based configuration. The dictionary contains mappings of configuration values that are used to specify behavior and output for loggers.

# Configuration Format
The dictionary-based configuration has a specific format. Each logger and handler is represented by a dictionary. The root logger is represented with the key `root`. Loggers and handlers can define their own levels, filters, and formatters.

Here is an example of a basic configuration dictionary:
```
{
    'version': 1,
    'handlers': {
        'console': {
            'class': 'logging.StreamHandler',
            'level': 'DEBUG',
            'formatter': 'simple'
        }
    },
    'loggers': {
        'my_module': {
            'level': 'DEBUG',
            'handlers': ['console']
        }
    },
    'root': {
        'level': 'INFO',
        'handlers': ['console']
    },
    'formatters': {
        'simple': {
            'format': '%(asctime)s - %(name)s - %(levelname)s - %(message)s'
        }
    }
}
```

# Example Usage
To use the `logging.config.dictConfig` method with the configuration dictionary, you can do the following:
```
import logging.config

config = {
    # configuration dictionary
}

logging.config.dictConfig(config)

logger = logging.getLogger('my_module')
logger.debug('Debug message')
```

Here, the `dictConfig` method is used to configure the logging module with the `config` dictionary defined earlier. Then, a logger for the `my_module` module is retrieved using the `getLogger` method. Finally, a debug message is logged using the `debug` method on the logger instance.

# Conclusion
With `logging.config.dictConfig`, you can easily configure logging behavior and output using a dictionary-based configuration. The configuration format is simple and flexible, allowing customization of settings for loggers and handlers.
