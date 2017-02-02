Doorbell
========

## Phase 1
* Lambda endpoints for all actions
* Web portal for management
* Per-entry notification settings
* Reply message "Grant Ed"/"Dan Eyed"

## Diagram
Call -> menu.xml

## URLs
* http://static.grantcohoe.com/cloudbell/menu.xml (main menu)
* http://static.grantcohoe.com/cloudbell/connect.xml (Connect GV-style to phones)
* http://static.grantcohoe.com/cloudbell/letin.xml (Play DTMF tone and notification)
* http://twimlets.com/menu?Message=Enter%20access%20code%20or%20press%201%20to%20be%20connected&amp;Options%5B1%5D=http%3A%2F%2Fstatic.grantcohoe.com%2Fcloudbell%2Fconnect.xml&amp;Options%5B3425%5D=http%3A%2F%2Fstatic.grantcohoe.com%2Fcloudbell%2Fletin.xml&amp;

/code
  * POST (create new code and associate it with a person)
/code/{id}
  * GET (retrieve a code and its associated data)
  * PUT (modify)
  * DELETE (delete)
/auth/{id}
  * POST (access the door)
    * 200: Success
    * 403: Failure
