20 signs your AI-generated code is already COMPROMISED

Here's what's killing in your codebase ( RIGHT NOW )

1/ your .env was committed at any point in git history
> "deleted" files stay in git history forever
> rotate every key in that file. every single one.

2/ you use SELECT * on user tables in public API responses
> password hashes, internal flags, admin roles
> all returned to the frontend. right now.

3/ admin routes have no server-side role check
> being logged in is not the same as being authorized
> anyone with a valid session can hit that route

4/ your JWT secret is "secret" or matches a tutorial
> attackers test common secrets
> this one is already on wordlists

5/ error responses include file paths or table names
> a complete map of your infrastructure
> handed to anyone who sends a bad request

6/ CORS allows * in production
> any website can make requests to your API
> with your users' cookies attached

7/ user A can access user B's data by changing an ID in the URL
> IDOR vulnerability
> extremely common in AI-generated code. easy to miss.

8/ /login has no rate limiting
> brute force runs completley unchecked
> no throttle, no lockout, no friction

9/ passwords stored as MD5 or SHA1
> both cracked trivially with rainbow tables
> not acceptable in 2026

10/ npm packages haven't been audited since initial install
> run `npm audit`
> count the criticals. fix them.

11/ non-standard ports publicly accessible
> redis on 6379 or DB on 5432
> shouldn't be reachable from the internet

12/ API keys visible in the browser network tab
> they're in the frontend bundle
> available to anyone who opens devtools

13/ your server process runs as root
> full system compromise if the app is exploited
> one vulnerability and it's everything

14/ file uploads accept any MIME type
> upload a server-side script
> execute it. full access.

15/ SQL queries use string interpolation
> `"SELECT * FROM users WHERE name = '" + name + "'"` 
> textbook SQL injection. still happening in 2026.

16/ sessions valid indefinitely
> stolen token from 6 months ago still grants full access
> no expiry = no control

17/ HTTP works in production without redirecting to HTTPS
> credentials sent in plaintext
> on any network, by anyone watching

18/ no Content Security Policy header
> XSS attacks can load scripts from anywhere
> one line of config prevents this

19/ no monitoring or alerting set up
> a breach may have already happened
> you'd only know when a user emails you

20/ internal services trust anything on the same network
> one compromised service = everything accessible
> lateral movement is how breaches scale

most vibe coded apps i've reviewed had 8 to 12 of these.

run this audit before you ship. bookmark it for every new project.