=====================================
Equivalent Pharmaceutical ID Standard
=====================================

The Equivalent Pharmaceutical ID (EPID) outlines how EPID data is formatted.

--------
Overview
--------

The EPID Standard defines how medications and equivalent medications are 
defined and named.

A **medication** refers to a single pharmaceutical product for medical use. It
may include one or more ingredients and a single dosage form. Ingredients have 
a single strength.

A group of medications are grouped under an **equivalent medication**. All
medications under an equivalent medication will have the same ingredients and
strengths. There may be one or more dosage forms.

------------
Introduction
------------

The EPID Standard follows the following guiding principles for development:

- All medications under an **equivalent medication** group are assumed 
  therapeutically, clinically, and legally interchangeable.

- Whenever conflicts arise in priorities, the decision that improves the 
  use and application of the EPID by end users (i.e. health care 
  professionals) takes priority.

Ingredients
===========

**Ingredients** are a single pharmaceutical molecule used for medical 
purposes. The following are the naming conventions for ingredients:

- Wherever possible, the International Nonproprietary Names (INN) is used for
  the naming of ingredients.
  
- Exceptions are made for cases where the INN complicates the EPID and add 
  no additional value. For example, ``levothyroxine sodium`` (INN) would be 
  changed to ``levothyroxine`` as the ``sodium`` component adds no additional
  value or clarity to the ingredient.

- Ingredients take the most concise naming possible. Bases, esthers, salts, 
  etc. should only be included in the ingredient name if they add necessary
  clarity between closely related ingredients. For example, 
  ``pantoprazole sodium`` and ``pantoprazole magnesium`` would be used as both
  salts have distinct pharmacokinetic properties.

- Ingredients may include additional names for localization purposes. For 
  example, the ``paracetamol`` ingredient record will use ``paracetamol`` as 
  its ``name`` and ``acetaminophen`` for its ``name_ca`` value.
  
- Ingredients are displayed in lower case.

  - Exception: letters may be capitalized in cases where the letter is 
    commonly capitalized (e.g. ``onabotulinumtoxinA``)

Strengths and Units
===================

A **strength** is include with all ingredients. This following are conventions
used for strengths:

- The most commonly used unit is chosen for the EPIC record.

- In cases where two units may be used (e.g. ``1000 mg`` or ``1 g``), the more
  precise unit will be used (``1000 mg`` in the previous example).

- Ingredients that make use of concentrations will be represented per 1 unit
  volume (e.g. ``per 1 mL``).

  - Exception: for concentrations where only one dose is ever given (e.g. a 
    vaccine always given at 0.5 mL); these will be represnted by the the 
    administered volume.

Dosage Forms
============

A single **dosage form** are associated with every medication record and 
multiple **dosage forms** may be associated with an equivalent medication
record.

The following are conventions used for dosage forms:

- Dosage forms are reduced to the simplest encompassing description possible.

- Descriptions of dosage forms that do not significantly impact the clinical
  application of a dosage form are not included. For example, ``gel capsule``
  would be reduced to ``capsule``.

- References to short acting formulations (e.g. ``immediate release``) are not
  included; it is assumed a formulation is short acting unless otherwise 
  stated.

- Long-acting formulations (e.g. ``sustained release``, 
  ``extended release``) are represented as ``long acting`` following the 
  dosage form.

----------
Versioning
----------

The EPID uses a MAJOR.MINOR versioning system. Versions refer to the EPID
Standard and **not** updates to the actual EPID data. Between minor versions,
there should be minimal changes required by the end user. Between major 
versions, there will be moderate to significant changes required by the end 
user.
