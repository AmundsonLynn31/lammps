.. index:: fix nve
.. index:: fix nve/intel
.. index:: fix nve/kk
.. index:: fix nve/omp

fix nve command
===============

Accelerator Variants: *nve/intel*, *nve/kk*, *nve/omp*

Syntax
""""""

.. parsed-literal::

   fix ID group-ID nve

* ID, group-ID are documented in :doc:`fix <fix>` command
* nve = style name of this fix command

Examples
""""""""

.. code-block:: LAMMPS

   fix 1 all nve

Description
"""""""""""

Perform constant NVE integration to update position and velocity for
atoms in the group each timestep.  V is volume; E is energy.  This
creates a system trajectory consistent with the microcanonical
ensemble.

----------

.. include:: accel_styles.rst

----------

Restart, fix_modify, output, run start/stop, minimize info
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

No information about this fix is written to :doc:`binary restart files <restart>`.  None of the :doc:`fix_modify <fix_modify>` options
are relevant to this fix.  No global or per-atom quantities are stored
by this fix for access by various :doc:`output commands <Howto_output>`.
No parameter of this fix can be used with the *start/stop* keywords of
the :doc:`run <run>` command.  This fix is not invoked during :doc:`energy minimization <minimize>`.

Restrictions
""""""""""""
 none

Related commands
""""""""""""""""

:doc:`fix nvt <fix_nh>`, :doc:`fix npt <fix_nh>`

Default
"""""""

none
