# SSH to CCC from ACE-VNC

From some reason, using the regular workflow of adding the ssh key to the CCC hosts does not work when you try to do it from the ACE machines, a different (working) approach is:

1. Create a key:

   ```bash
   ssh-keygen -t rsa
   ```

2. Copy your key from `vi ~/.ssh/id_rsa.pub` 

3. Log in to one of the old machines:

   ```bash
   ssh <ccc-user-ID>@dccxl001.pok.ibm.com
   ```

4. Paste the key that you copied in to `~/.ssh/authorized_keys`

You will now be able to access both the new and old machines without a password

