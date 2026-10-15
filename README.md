THE Bookified application

Features 
What happens, in plain words:
1. You upload a PDF. Your browser reads the text out of it and draws page 1 as a cover picture.
2. The PDF and cover are stored in Vercel Blob, an online file store.
3. The book's details, and its text cut into chunks of about 500 words ("segments"), are saved in MongoDB, a database.
4. On the book's page you click the microphone. Vapi, a voice-AI service, starts a call and speaks with an ElevenLabs voice.
5. When the AI needs facts from the book, Vapi calls your app at /api/vapi/search-book. That route searches the segments and sends the matching text back.
6. Clerk handles sign-in and subscription plans (free, standard, pro). Plans limit how many books and voice sessions you get.