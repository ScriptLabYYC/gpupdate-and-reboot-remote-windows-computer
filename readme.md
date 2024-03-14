$HOSTNAME = read-host Please enter host name of windows PC!
write-host Running GPUpdate /Force ; invoke-command -ComputerName $HOSTNAME -ScriptBlock {gpupdate /force}
write-host Rebooting ; invoke-command -ComputerName $HOSTNAME -ScriptBlock {shutdown -t 0 -r}
