# ESAPI-CBCTmoves
ESAPI standalone that mines Aria for all CBCT moves

This standalone Eclipse Scripting Application PlugIn (ESAPI) code for C# sharp was developed to allow CBCT online verification moves to be determined on mass for patients very quickly. It accesses 1 patient plan at a time, skips various courses and plans that don't meet strict criteria then determines all the CBCT imaging moves for that plan until no patients and plans remain. The code returns results in .csv format and includes but is not limited to vertical, lateral and longitudinal shifts for each registration. 

The code has been validated against a group of over 100 stereotactic Lung treatments and a range of other sites. For the most part results are accurate but there are some exceptions. It is known to fail when a patients single CT scan is used for 2 different treatment sites where those plans both have CBCT as registations are linked by the images Frame of Reference which isn't unique for these cases. The code automatically returns results outside of 2cm into a seperate csv for investigation, which catches these cases. 

Current contributors:
1. Castle Hill Hospital - main developers.
