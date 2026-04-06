Secure Login System (or… how I stopped trusting plain text passwords)

Why I built this

One random night, I was reading about data breaches.  
Millions of passwords leaked. Again.

And the scary part?  
Most of them weren’t stolen with genius hacking…  
They were just poorly stored.

That didn’t sit right with me.

So I decided to build something simple but meaningful:  
 A login system where even if things go wrong… user data stays safe.

 The idea

This project is not just a login form.  
It’s a gatekeeper that treats user credentials like secrets, not data.

I wanted to answer one question:

“If someone breaks into my database… what will they actually get?”

And the answer should be:  
Nothing useful.



How I approached security

I didn’t try to reinvent security.  
I followed what actually works in the real world.

 I never store your password
When you register, your password is transformed using bcrypt into something unreadable.

Even I can't reverse it.  
Even if the database leaks, attackers just see gibberish.



No tricks allowed (SQL Injection protection)
Hackers often try inputs like:
Instead of trusting raw queries, I used SQLAlchemy,  
so the system treats input as data, not commands.


Logged in? You get a secure pass
After login, the system creates a session.

Think of it like a signed VIP pass:
- You don’t re-enter your password every time  
- No one can fake it  
- It expires safely  



What I used

- Python → the brain  
- Flask → the skeleton  
- Flask-Bcrypt → password protection  
- Flask-Login → session management  
- SQLite → lightweight database  


 Run it yourself

 bash
git clone https://github.com/puneethgoud733-pixcel/secure-login-system.git
cd secure-login-system