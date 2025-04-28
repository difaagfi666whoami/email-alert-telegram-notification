This is a self-taught project that I am currently building to make mail-checking activities became easier and fast.  

When you type in Telegram:
“Please find the email related to "GMO" with the error message today.”,

The bot will:
- Aggregate all today’s error messages
- Summarize the grouped messages
- Highlight unusual/rare messages
- Send the AI-generated summary back to Telegram

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
How does this work? 
1. Using IMAP as an email data resource.
2. Using Python to fetch data information from IMAP. such as msg_id, sender, subject, body content, time_received.
3. Run the code/back-end process using Amazon Web Services (Lambda + S3, personal account: free tier). Because I want to run the code on a serverless platform.
4. Sent the fetched email data to Neon PostgreSQL. PostgreSQL is the main database and it was created on a serverless cloud (free tier).
5. Simply using N8N to make a specific workflow, such as email summary using AI, telegram alert notification (and much more, we can leverage this workflow depending on the ideas we want to create)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
