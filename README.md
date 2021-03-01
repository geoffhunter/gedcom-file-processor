# gedcom-file-processor

A utility to produce lists of individuals, families and children, from a GEDCOM format file. These lists are used by the gedcom-reporter, gedcom-website-builder and gedcom-splitter utilities.

Overview

This utility allows the user to produce lists of individuals, families and children, from a GEDCOM format file.

Modules

gedcom_file_processor.pyw

The main module. This module presents the user with a Windows user interface, allowing them to edit parameters, and process a GEDCOM format file.

Parameters used in this package are:

GED File	The name of the GEDCOM format file to be processed. The file should be in the location where the utility runs.

ged_lib.py

This module contains parameter variables and lists used by other modules and the following subroutines:

get_params reads parameter values from params.txt.

save_params writes parameter values to params.txt.

edit_params presents the user with a user interface to edit parameters.

process_ged_file reads the GEDCOM file specified as a parameter and produces Individuals.txt, Families.txt and Children.txt containing lists of individuals, families and children, with attributes.

read_individuals reads Individuals.txt into the ‘individuals’ list.

write_individuals writes the ‘individuals’ list to Individuals.txt.

add_individual writes an individual to the ‘individuals’ list.

get_person_name returns the name of the individual (id passed as a parameter) in the form ‘surname, forename(s)’.

get_birth_date returns the year of birth of the individual (id passed as a parameter) in form ‘b. yyyy’.

get_family_where_child returns the id of the family where the individual (id passed as a parameter) is a child.

read_families reads Families.txt into the ‘families’ list.

add_family writes a family to the ‘families’ list.

write_families writes the ‘families’ list to Families.txt.

get_father_id returns the id of the husband in the family where the individual (id passed as a parameter) is a child.

get_mother_id returns the id of the wife in the family where the individual (id passed as a parameter) is a child.

read_children reads Children.txt into the ‘children’ list.

add_child writes a child to the ‘children’ list.

write_children writes the ‘children’ list to Children.txt.
