# CS 260 Notes

[My startup - Neckvana] (https://github.com/N-C-04/startup.git)

## Helpful links

- [Course instruction](https://github.com/webprogramming260)
- [Canvas](https://byu.instructure.com)
- [MDN](https://developer.mozilla.org)


## Git & GitHub Setup
- Learned how to create a repository from a course template on GitHub.
- Practiced cloning a repository to a local folder outside OneDrive to avoid sync issues.
- Reviewed basic Git commands: `git add`, `git commit`, `git push`, and `git pull`.
- Confirmed how to check repository status with `git status`.

## Markdown Basics
- Headings are created with `#` symbols.
- Lists can be unordered (`-`) or ordered (`1.`).
- Links use `[text](URL)` format.
- Images use `![alt text](image.png)` format.

## Startup Idea – Neckvana
- A next‑generation travel neck pillow for comfort, portability, and style.
- Key features: ergonomic 360° support, compact design, breathable cover, optional smart posture sensor.
- Potential technologies: HTML/CSS for landing page, React for customization tool, backend service for orders, database for user profiles, WebSocket for live chat.


## AWS

My IP address is: 54.81.96.130
Launching my AMI I initially put it on a private subnet. Even though it had a public IP address and the security group was right, I wasn't able to connect to it.

## Caddy

No problems worked just like it said in the [instruction](https://github.com/webprogramming260/.github/blob/main/profile/webServers/https/https.md).

## HTML

This was easy. I was careful to use the correct structural elements such as header, footer, main, nav, and form. The links between the three views work great using the `a` element.

The part I didn't like was the duplication of the header and footer code. This is messy, but it will get cleaned up when I get to React.

## CSS

This took a couple hours to get it how I wanted. It was important to make it responsive and Bootstrap helped with that. It looks great on all kinds of screen sizes.

Bootstrap seems a bit like magic. It styles things nicely, but is very opinionated. You either do, or you do not. There doesn't seem to be much in between.

I did like the navbar it made it super easy to build a responsive header.

```html
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <a class="navbar-brand">
            <img src="logo.svg" width="30" height="30" class="d-inline-block align-top" alt="" />
            Calmer
          </a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" href="play.html">Play</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="about.html">About</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="index.html">Logout</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
```

I also used SVG to make the icon and logo for the app. This turned out to be a piece of cake.

```html
<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg">
  <rect width="100" height="100" fill="#0066aa" rx="10" ry="10" />
  <text x="50%" y="50%" dominant-baseline="central" text-anchor="middle" font-size="72" font-family="Arial" fill="white">C</text>
</svg>
```

## React Part 1: Routing

Setting up Vite and React was pretty simple. I had a bit of trouble because of conflicting CSS. This isn't as straight forward as you would find with Svelte or Vue, but I made it work in the end. If there was a ton of CSS it would be a real problem. It sure was nice to have the code structured in a more usable way.

## React Part 2: Reactivity

This was a lot of fun to see it all come together. I had to keep remembering to use React state instead of just manipulating the DOM directly.

Handling the toggling of the checkboxes was particularly interesting.

```jsx
<div className="input-group sound-button-container">
  {calmSoundTypes.map((sound, index) => (
    <div key={index} className="form-check form-switch">
      <input
        className="form-check-input"
        type="checkbox"
        value={sound}
        id={sound}
        onChange={() => togglePlay(sound)}
        checked={selectedSounds.includes(sound)}
      ></input>
      <label className="form-check-label" htmlFor={sound}>
        {sound}
      </label>
    </div>
  ))}
</div>
```
# CodePen Fork Notes
- Replaced <div> navigation with <a> anchor tags linking to BYU and FamilySearch.
- Updated <ul> list in the <section> to include: apples, bananas, oranges.
- Added an <img> tag inside <aside> using an external image URL and set the width attribute.
- Appended a new row to the <table> with: HTML, CSS, JavaScript.
- Inserted my name in an <h1> tag inside the <header>.
- Linked the <footer> to my GitHub repository.

# Caddy Setup Notes
- Learned how to locate and edit the Caddyfile in Ubuntu using nano and cd /etc/caddy.
- Discovered how to validate the Caddyfile with caddy validate and reload with sudo systemctl reload caddy.
- Used find / -name Caddyfile to locate missing config files.
- Realized I need sudo access to edit system files — will follow up with instructor or TA for credentials.
- Understood the structure of a proper Caddyfile block for serving multiple sites.

 I fixed my git error and made sure i always went to the HTML folder inside the startup folder

 ## HTML Component Pages

- Added `database.html` with a table showing sample stored data.
- Created `websocket.html` with a placeholder for real-time updates.
- Linked all pages together with navigation bars.
- Confirmed structure with header, nav, main, footer.

## Neckvana Homepage

- Built `index.html` to reflect Neckvana’s brand and features.
- Added navigation to all app components.
- Included SVG and placeholder content for posture tracking.
- Linked to GitHub repo and other pages.
