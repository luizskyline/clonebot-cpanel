# Clonebot Bot adapted for a shared hosting environment like cPanel

After setting up the Python app (using a subdomain), upload the files to the created folder via the file manager. Open the cPanel terminal and execute the path you received during the Python app setup:

source /home/username/virtualenv/botfolder/3.9/bin/activate && cd /home/username/botfolder

Run the following command to install the required packages:

python -m pip install -r requirements.txt

After the installation, exit the terminal. Go to the file manager, navigate to virtualenv/botfolder/3.9/lib/python3.9/site-packages/pyrogram/storage, and replace the file memory_storage.py to fix the error of pyrogram (struct.error: unpack requires a buffer of 271 bytes).

Return to the terminal and execute:

source /home/username/virtualenv/botfolder/3.9/bin/activate && cd /home/username/botfolder

Then run:

python main.py

DONE!

To keep the bot running 24/7, go to cron jobs and configure it with:

/home/username/botfolder/start.sh
""


</details>
