# To list all colors in 16-color mode

Reference <http://jafrog.com/2013/11/23/colors-in-terminal.html>

```
for code in {30..37}; do
  echo -en "\e[${code}m"'\\e['"$code"'m'"\e[0m";
  echo -en "  \e[$code;1m"'\\e['"$code"';1m'"\e[0m";
  echo -en "  \e[$code;3m"'\\e['"$code"';3m'"\e[0m";
  echo -en "  \e[$code;4m"'\\e['"$code"';4m'"\e[0m";
  echo -e "  \e[$((code+60))m"'\\e['"$((code+60))"'m'"\e[0m";
done
```
