Can't `ping localhost` or `ping 127.0.0.1` ?
- Answer: Check `sudo /usr/libexec/ApplicationFirewall/socketfilterfw --getstealthmode`
  If it's ON? That could be why. Because this prevents your machine answering ping.
  
- https://www.iljitsch.com/2022/12-27-cant-ping-your-mac-make-this-change.html

