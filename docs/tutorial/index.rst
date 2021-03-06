
Tutorials
---------------------

A High Level Glance
====================

.. image:: https://user-images.githubusercontent.com/1381301/29187907-2caaa740-7dc6-11e7-8220-e20ca52c3ca6.png


* ``DataFlow`` is a library to load data efficiently in Python.
  Apart from DataFlow, native TF operators can be used for data loading as well.
  They will eventually be wrapped under the same ``InputSource`` interface and go through prefetching.

* You can use any TF-based symbolic function library to define a model, including
  a small set of models within tensorpack. ``ModelDesc`` is an interface to connect the graph with the
  ``InputSource`` interface.

* tensorpack trainers manage the training loops for you.
  They also include data parallel logic for multi-GPU or distributed training.
  At the same time, you have the power of customization through callbacks.

* Callbacks are like ``tf.train.SessionRunHook``, or plugins. During training,
  everything you want to do other than the main iterations can be defined through callbacks and easily reused.

* All the components, though work perfectly together, are highly decorrelated: you can:

  * Use DataFlow alone as a data loading library, without tensorfow at all.
  * Use tensorpack to build the graph with multi-GPU or distributed support,
    then train it with your own loops.
  * Build the graph on your own, and train it with tensorpack callbacks.

User Tutorials
========================

.. toctree::
  :maxdepth: 1

  dataflow
  input-source
  efficient-dataflow
  symbolic
  trainer
  training-interface
  callback
  save-load
  summary
  faq

Extend Tensorpack
=================

.. toctree::
  :maxdepth: 1

  extend/dataflow
  extend/augmentor
  extend/model
  extend/callback
  extend/trainer

Notes
======
.. toctree::
  :maxdepth: 1

  performance-tuning
