# Use `su - {name}` Instead of `su {name}`

Using `su {name}`, while it does switch the user, does not initiate the
logon "scripts". For example, it will not initiate your bashrc. `su -
{name}` switches the user and initiates the logon scripts.
