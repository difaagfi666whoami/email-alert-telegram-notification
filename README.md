This is a self-taught project that I currently build to make mail-checking activities became easier and fast.  

When you type in Telegram:
“Please find email related to "GMO" with error message today”,

the bot will:
- Aggregate all today’s error messages
- Summarize the grouped messages
- Highlight unusual/rare messages
- Send the AI-generated summary back to Telegram

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
How this is works, 
1. Using IMAP as an email data resource.
2. Using python to fetch data information from IMAP. such as msg_id, sender, subject, body content time_received.
3. Run the code/back-end process using Amanzon Web Service (lambda + S3, personal account : free tier). Because I want to running the code on serverless platform.
4. Sent the fetched email data to Neon postgreSQL. postgreSQL is the main database and it was created on serverless cloud (free tier).
5. Simply using N8N to make spesified workflow such as email summary using AI, telegram alert notification (and much more, we can leverage this workflow depending on ideas we want to create)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
