# hr-ad-tools

This is intended to be used as a long term project to create a tool that can be used internally to allow members of HR or possibly other management users a self service method of disabling user accounts. The idea came from a recent immediate termination of an employee after hours and thinking we should look into possibilities of making this a process that can be done without direct immediate involvement of someone in IT.

Potential process:
-HR or other authorized end user log in
  -how to verify authorization? AD group membership likely desired method
-Once logged in user is presented with option to create or terminate user (beginning focus on termination)
-For termination have these fields required
  -user email
  -username (this might not be a realistic ask as usernames are truncated and that confuses people)
-Have a check run to return AD information based on inputs so that the submitter can verify the correct user is being targeted
-Once verified have information processed and the account disabled
  -create a file with necessary info that is processed via a powershell script on another server
  -file must include information necessary to disable the account as well as a record of who did the submission
