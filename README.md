# protocols
Collection of protocols for the Living Physics/Trappy-Scopes laboratory.

### Notes

1. **Cellculture maintainance process diagrams are obselete.**

2. **Experimental protocols/master protocols are updated regularly. The latest one should be used.**

	****

## List of protocols

+ cellculture
	+ streaking_plates.md
	+ **Other protocols, especially the process diagrams are obselete.**
+ microfluidics
  + preparation
  	+ bsa_treatment.md (also deals with stock solution prepration)
  + fabrication
  	+ clean_glassslides_prep.md
  	+ piranha_solution_prep.md
  	+ scotchtape_circles_prep.md
+ mediaprep
  + tapp_media.md (also included Acetate minimal media TAP+P-Ac)
  + agar_plates.md          
  + ampicillin_media.md     
  + stocksol_prep.md    

## Schema for writing protocols

The protocols should be written in markdown format and should strictly follow this schema. Adhere to the **headings** strictly.

1. Schema:
	```markdown
	---
	author: TrappyUser
	editor: Another TrappyUser
	description: blah blah
	references: blah blah
	---
	
	# Title of the protocols
	
	1. Preamble text line 1
	2. Preamble text line 2
	3. ...
	
	## Requirements
	
	1. Requirement 1
	2. Requirement 2
	3. ...
	
	## Steps
	
	### Macro step 1
	1. Macro step definations are optional
	2. ...
	
	### Macro step 2
	1. ...
	2 ...
	
	## Additional Information
	
	Also optional, but useful.
	```
	
2. Use lists (itemized or enumerated) as much as possible, since lists are easier to parse and format.
