# gtui - generalized text user interface

put gtui in your $PATH and make it executable

Example script that uses gtui:
```bash
# Define items (you could read these from a file):

items=$(cat <<EOF
apples 4
oranges 2
potatoes 1
coffee 0
EOF
)

# Define keybindings, using special key names as per the new mapping
binds=$(cat <<EOF
j scroll_down "[j] Down"
k scroll_up "[k] Up"
Return select_item "[Enter] Select"
q quit "[q] Quit"
e scroll_down
EOF
)

# Call gtui with the defined items and keybindings
./gtui "$items" "$binds"
```
