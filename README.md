🛒 Amazon Price Tracker 

Ever wished your favorite Amazon product would magically tell you when it’s on sale? Well… now it can! This Python script tracks the price of your chosen product and sends you an email alert when it drops below your set “BUY NOW” price.

⚡ Features

Tracks any Amazon product automatically.

Sends instant email alerts when the price drops.

Fully customizable: product link , desired price , your email . ✅

Can run daily like a boss using Task Scheduler or Cron.

Setup
1. Clone the repo
git clone <your-repo-url>
cd <repo-folder>

2. Install dependencies
pip install requests beautifulsoup4 python-dotenv

3. Add your secret sauce (.env)

Create a .env file in the project folder:

EMAIL_ADDRESS=your_email@example.com
EMAIL_PASSWORD=your_email_password
SMTP_ADDRESS=smtp.example.com


⚠️ Important: Use your own email & password!

Gmail Users – 2-Step Verification & App Password

If you use Gmail, you must enable 2-Step Verification on your account:

Go to your Google Account → Security → 2-Step Verification → Turn it ON.

Generate an App Password (choose “Mail” → “Other”) and copy it.

Use this app password as EMAIL_PASSWORD in your .env file.

This makes your account more secure and allows Python to send emails safely. 

4. Customize the script

Product link – swap in your favorite Amazon URL:

url = "https://www.amazon.com/dp/YOUR_PRODUCT_LINK_HERE"


Target price – set your “BUY NOW” price:

BUY_PRICE = 100  # Change this to your magic number

5. Run it manually (test mode)
python amazon_price_tracker.py


If your product is cheaper than BUY_PRICE, BOOM 💥 you get an email.

6. Automate the magic 
Windows – Task Scheduler

Open Task Scheduler → Create Basic Task → Name it.

Trigger → Daily → Pick a time.

Action → Start a Program → Browse → Your Python executable.

Add argument → path to your script:

"C:\Users\You\amazon_price_tracker.py"


Done! Your script now checks prices daily and emails you when it’s deal time. 🎯

Linux/Mac – Cron Job
crontab -e


Add:

0 9 * * * /usr/bin/python3 /home/user/amazon_price_tracker.py


This runs it every day at 9 AM – like a digital shopping genie. 🧞‍♂️

⚡ Notes

Update .env with your actual credentials.

Change the Amazon link whenever you fall in love with a new product.

If emails don’t arrive, check SMTP, credentials, and app password.

💡 Now sit back, sip coffee ☕, and let Python grab your dream deals for you!
