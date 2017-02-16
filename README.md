var=${user_info[0]:1}
          FNAME="$(tr '[:lower:]' '[:upper:]' <<< ${user_info[0]:0:1})"
          LNAME="$(tr '[:lower:]' '[:upper:]' <<< ${var:0:1})${var:1}"
          sed "s/{UID}/${user_info[0]}/g;
          s/{PASSWORD}/${user_info[1]}/g;
          s/{FIRST_NAME}/${FNAME}/g;
          s/{LAST_NAME}/${LNAME}/g;
