## out of scope path
* out_of_scope
  - utter_out_of_scope

## help
* help
  - utter_help

## thank
* thank
  - utter_welcome

## happy path
* greet
  - utter_greet
  - utter_help

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot


## incident form
* open_incident OR password_reset OR problem_email
    - open_incident_form
    - form{"name": "open_incident_form"}
    - form{"name": null}

## incident form interrupted
* open_incident OR password_reset OR problem_email
    - open_incident_form
    - form{"name":"open_incident_form"}
* help
    - utter_help
    - open_incident_form
    - form{"name":null}

## incident form interrupted
* open_incident OR password_reset OR problem_email
    - open_incident_form
    - form{"name":"open_incident_form"}
* out_of_scope
    - utter_out_of_scope
    - open_incident_form
    - form{"name":null}

## incident status
* incident_status
    - action_incident_status
    - utter_ask_whatelse

## open incident form switch to incident status
* open_incident OR password_reset OR problem_email
    - open_incident_form
    - form{"name":"open_incident_form"}
* incident_status
    - action_incident_status
    - open_incident_form
    - form{"name":null}

## explain priority
* open_incident OR password_reset OR problem_email
    - open_incident_form
    - form{"name":"open_incident_form"}
    - slot{"requested_slot": "priority"}
* explain
    - utter_explain_priority
    - open_incident_form
    - form{"name":null}