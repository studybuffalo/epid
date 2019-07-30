=====================================
Equivalent Pharmaceutical ID Standard
=====================================

|Version|

.. |Version| image:: https://img.shields.io/badge/EPID%20Standard-1.0-blue
   :alt: EPID Standard Version 1.0

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

- Ingredients take the most concise naming possible. Bases, esters, salts,
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

- Units are represented in metric and use the formating as outlined by the
  International System of Units (SI units).

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

- Units are always separated from the numeric value by a single space
  character (e.g. ``1 mg``).

  - **Exception:** percents (``%``) immediately follow the number
    (e.g. ``1%``)

Medications
===========

**Medication** records are the sum of the ingredient(s), strength(s), and
dosage form for a pharmaceutical product. Each individual component can be
individually referenced by the medication ID. Each medication record also
contains a name that is the sum of all components.

The following conventions are used for medication names:

- A medication name is made up of an ingredient name, followed by the
  strength and the dosage form (e.g. ``acetaminophen 500 mg table``).

- In cases where a medication have multiple ingredients:

  - Each ingredient and strength pair are listed and separated by an asterisk
    before the dosage form (e.g.
    ``codeine 60 mg * acetaminophen 500 mg tablet``).

  - In most cases, ingredients will be listed in alphabetical order, with the
    following exceptions:

    - Ingredients with clinical effects are listed before other ingredients
      that do not exert a clinical effect (e.g. ``amoxicillin`` would be
      listed before ``clavulanate``).

    - Combinations including opioids (including tramadol) will list the opioid
      as the first ingredient (e.g.
      ``codeine 30 mg * caffeine 15 mg * acetaminophen 325 mg``)

    - Combinations including acetaminophen will list the other ingredients
      before the acetaminophen component (e.g.
      ``pseudoephedrine 30 mg * acetaminophen 500 mg tablet``).

Equivalent Medications
======================

**Equivalent medication** records are groups of **medication** records that
denote clinically and (generally) legally equivalent products. Each individual
medication can be the equivalent medication ID. Each equivalent medication
record also contains a name that summarizes all medication components.

The following conventions are used for the equivalent medication name:

- Ingredients and strengths follow the same standards as a medication record.

- Dosage forms are groups together alphabetically and separated by a slash
  (``/``) with no spaces on either side (e.g. ``capsule/tablet``).

----------
Versioning
----------

The EPID uses a MAJOR.MINOR versioning system. Versions refer to the EPID
Standard and **not** updates to the actual EPID data. Between minor versions,
there should be minimal changes required by the end user. Between major
versions, there will be moderate to significant changes required by the end
user.
