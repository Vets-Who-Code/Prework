# Module 6: Capstone — Your Portfolio

**⏱ Estimated Time: 8-12 hours**

---

## The Goal

Everything you've learned comes together here.

Your capstone is a **personal portfolio website about you** — your story, your background, your journey into tech. It's not a generic project everyone builds the same way. It's yours.

This portfolio will:
- Demonstrate every skill from the pre-work
- Serve as a real asset when job hunting
- Be discussed in detail during your interview

**You will walk through every line of code with our team. Be prepared to explain your decisions and make modifications on the spot.**

---

## Required Pages

Your portfolio must have these four pages:

### 1. Home

Your landing page. First impressions matter.

**Must include:**
- Hero section with your name and a brief introduction
- Navigation that works on both mobile and desktop
- Clear visual hierarchy
- Smooth user experience

### 2. About

Your story. Who you are, where you've been, where you're going.

**Must include:**
- Your background (military service, previous career, etc.)
- Why you're pursuing software engineering
- What drives you
- **Your setup proof** — screenshots showing:
  - Your terminal with custom aliases configured
  - Your VS Code with extensions installed
  - Your GitHub profile with commit history

These screenshots prove you completed the earlier modules.

### 3. Projects

Showcase your work.

**Must include:**
- **Projects stored as data** in a JavaScript array of objects
- **Cards rendered dynamically** to the DOM using JavaScript (not hardcoded HTML)
- At minimum, your practice layouts from Module 4
- Links to live demos and GitHub repos

**This section must be built with JavaScript.** When we look at your code, we should see an array of project objects and a function that renders them.

### 4. Contact

How people can reach you.

**Must include:**
- Working contact form using Formspree
- Client-side form validation before submission
- Links to your GitHub and LinkedIn
- Professional email address

---

## Required Features

Your portfolio must include interactive features that demonstrate your JavaScript skills.

**Implement at least 5 of the following 8 features.**

Each feature description tells you what skill it demonstrates. The specific implementation is your creative decision.

---

### Feature 1: Theme Persistence

**Demonstrates:** DOM manipulation, event listeners, localStorage, CSS custom properties

**Requirements:**
- User can change a visual aspect of the site (colors, theme, layout preference)
- Their preference persists when they close and reopen the browser
- The change applies instantly without page reload

**Example implementations:**
- Dark/light mode toggle
- Color scheme selector
- Font size preference

---

### Feature 2: Responsive Navigation

**Demonstrates:** classList manipulation, event handling, responsive JavaScript

**Requirements:**
- Navigation adapts between mobile and desktop layouts
- Mobile navigation requires JavaScript interaction to open/close
- Smooth transitions between states
- Closes when a link is clicked (on mobile)

**The key:** This isn't just CSS media queries. The mobile menu must use JavaScript to toggle open/closed.

---

### Feature 3: Dynamic Content Rendering

**Demonstrates:** Arrays of objects, iteration methods, template literals, DOM creation

**Requirements:**
- Content stored as structured data in JavaScript (not hardcoded HTML)
- Data rendered to the page using JavaScript
- Adding new items to the data array automatically updates the page

**This is required for your Projects section.** You may also use it for skills, testimonials, timeline, etc.

Example data structure:
```javascript
const projects = [
  {
    id: 1,
    title: "Project Name",
    description: "What it does",
    technologies: ["HTML", "CSS", "JavaScript"],
    liveUrl: "https://...",
    repoUrl: "https://github.com/..."
  },
  // more projects...
];
```

---

### Feature 4: Content Filtering or Sorting

**Demonstrates:** Array filter/sort methods, event delegation, conditional rendering

**Requirements:**
- User can filter or sort displayed content by some criteria
- The view updates dynamically based on selection
- User can reset to see all content

**Example implementations:**
- Filter projects by technology/category
- Sort projects by date or name
- Filter skills by category

---

### Feature 5: Form Validation

**Demonstrates:** Form handling, validation logic, error states, DOM updates

**Requirements:**
- Form validates input before submission
- User sees clear error messages for invalid input
- Form only submits when all validation passes
- Validation happens on submit (real-time feedback is optional)

**Validation rules to implement:**
- Name: Required, minimum length
- Email: Required, valid format
- Message: Required, minimum length

---

### Feature 6: Animated Text or Elements

**Demonstrates:** setInterval/setTimeout, string manipulation, DOM updates over time

**Requirements:**
- Text or elements animate or change over time using JavaScript
- Animation is controlled programmatically (not just CSS animations)
- Animation can be stopped, started, or reset (or runs once on load)

**Example implementations:**
- Typing effect on hero headline
- Rotating titles ("I'm a developer / designer / problem solver")
- Counter animation for statistics

---

### Feature 7: Randomized Content

**Demonstrates:** Arrays, Math.random, event handling, dynamic updates

**Requirements:**
- Some content displays randomly from a collection
- User can trigger new random content (or it changes automatically)
- The same item doesn't repeat consecutively

**Example implementations:**
- Random quote or tip display
- Randomized fun facts about yourself
- Random project highlight

---

### Feature 8: Scroll-Based Interactions

**Demonstrates:** Scroll events, element positioning, conditional logic

**Requirements:**
- Something changes based on scroll position
- Uses JavaScript scroll event handling
- Smooth and performant

**Example implementations:**
- Header style changes on scroll (shrinks, changes color)
- Back-to-top button appears after scrolling
- Active section highlighting in navigation
- Fade-in animations as elements enter viewport

---

## Technical Requirements

### Code Quality

Your code should be:
- **Organized** — Logical file structure, related code grouped together
- **Readable** — Clear variable and function names
- **Commented** — Explain complex logic, document functions
- **Consistent** — Same formatting throughout

### File Structure

```
portfolio/
├── index.html
├── about.html
├── projects.html
├── contact.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── images/
    ├── screenshot-terminal.png
    ├── screenshot-vscode.png
    ├── screenshot-github.png
    └── ...
```

You can organize differently, but keep it logical.

### Responsive Design

Your site must work on:
- Mobile phones (320px and up)
- Tablets (768px and up)
- Desktops (1024px and up)

Test on multiple screen sizes. Use Chrome DevTools device toolbar.

### Performance

- Optimize images (compress, use appropriate sizes)
- Don't load unnecessary resources
- Test that pages load quickly

### Accessibility Basics

- All images have alt text
- Form inputs have labels
- Color contrast is sufficient
- Site is navigable with keyboard

---

## Building Your Portfolio: Step by Step

### Step 1: Plan

Before writing code, decide:
- What's your visual style? (colors, fonts, mood)
- What features will you implement?
- What content goes on each page?
- What projects will you showcase?

Sketch out your layouts on paper first.

### Step 2: Structure

Build the HTML structure for all pages:
- Set up your file structure
- Create all HTML files with semantic markup
- Add placeholder content
- Link CSS and JavaScript files

### Step 3: Style

Build out your CSS:
- Start with mobile styles first
- Add a CSS reset
- Define your CSS custom properties (colors, fonts, spacing)
- Style each section
- Add media queries for larger screens

### Step 4: Functionality

Add JavaScript features:
- Start with dynamic rendering (projects)
- Add navigation toggle
- Implement your chosen features one at a time
- Test each feature thoroughly

### Step 5: Polish

Refine everything:
- Check responsive behavior at all sizes
- Test all interactive elements
- Verify form submission works
- Add final content and images
- Comment your code

### Step 6: Deploy

Get it online:
1. Push to GitHub
2. Enable GitHub Pages in repository settings
3. Test the live site
4. Check all links work

---

## Deployment to GitHub Pages

### Step 1: Create Repository

On GitHub:
1. Click "New repository"
2. Name it (e.g., "portfolio" or "yourusername.github.io")
3. Make it public
4. Don't initialize with README (you have code already)

### Step 2: Push Your Code

```bash
cd your-portfolio-folder
git init
git add .
git commit -m "Initial portfolio"
git remote add origin git@github.com:yourusername/portfolio.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to repository Settings
2. Scroll to "Pages" section
3. Under "Source", select "main" branch
4. Click Save
5. Wait a few minutes

Your site will be live at:
`https://yourusername.github.io/portfolio`

Or if you named the repo `yourusername.github.io`:
`https://yourusername.github.io`

### Step 4: Verify

- Visit your live URL
- Test all pages and features
- Check on mobile
- Verify form submission

---

## Submission Checklist

Before submitting, verify:

### Pages
- [ ] Home page exists with hero and navigation
- [ ] About page tells your story and includes setup screenshots
- [ ] Projects page renders projects dynamically from JavaScript
- [ ] Contact page has working form with validation

### Features (at least 5)
- [ ] Theme persistence
- [ ] Responsive navigation with JavaScript
- [ ] Dynamic content rendering
- [ ] Content filtering or sorting
- [ ] Form validation
- [ ] Animated text or elements
- [ ] Randomized content
- [ ] Scroll-based interactions

### Technical
- [ ] Site is responsive (mobile, tablet, desktop)
- [ ] All links work
- [ ] Contact form submits via Formspree
- [ ] Images are optimized
- [ ] Code is clean and commented

### Git
- [ ] Repository has 20+ meaningful commits
- [ ] Commit messages are clear
- [ ] No unnecessary files committed

### Live Site
- [ ] Deployed to GitHub Pages
- [ ] All features work on live site
- [ ] Tested on multiple devices/browsers

---

## The Interview

After you submit, you'll be scheduled for a technical interview.

### What to Expect

The interview is a conversation about your work, not a test designed to trip you up.

**We will:**
- Ask you to share your screen
- Walk through your portfolio together
- Ask you to explain specific code sections
- Ask why you made certain decisions
- Possibly ask you to make a small modification

**We're looking for:**
- Understanding of your own code
- Ability to explain technical concepts
- Problem-solving approach
- Communication skills

### How to Prepare

1. **Review your code** — Make sure you understand every line
2. **Know your features** — Be ready to explain how each one works
3. **Practice explaining** — Talk through your code out loud
4. **Know the concepts** — Review the module material
5. **Be ready to code** — You might modify something live

### Common Questions

- "Walk me through how this function works"
- "Why did you choose this approach?"
- "What happens when a user clicks this?"
- "How would you add [feature] to this?"
- "What was the hardest part of building this?"
- "If you had more time, what would you improve?"

---

## After Submission

### Possible Outcomes

**Approved** — Welcome to the Hashflag Stack. We're excited to have you.

**Revisions Needed** — You're close. We'll provide specific feedback on what to address. Fix the issues and resubmit.

**More Preparation Recommended** — Additional foundation work would help you succeed. We'll suggest resources and welcome you to reapply when ready.

### Preparing for Day 1

If approved:

- Review your pre-work — Everything builds on this foundation
- Rest — The program is intense
- Set up your schedule — 20-24 hours per week for 17 weeks
- Tell your family — They need to know you'll be busy
- Show up ready to work

---

## Submission

When your portfolio is complete and deployed:

**Email:** hello@vetswhocode.io

**Subject:** Pre-Work Submission: [Your Name]

**Include:**
- Your live portfolio URL
- Your GitHub repository URL
- Brief note about which features you implemented

---

## Final Thoughts

Completing this pre-work represents a significant accomplishment. You've put in 40-60 hours of focused learning—more preparation than many programs require.

The Hashflag Stack will be challenging. The pace is faster, and the material goes deeper. But you've already demonstrated the discipline and capability to handle it.

**You've done the work. You're ready for what's next.**

---

<div align="center">

### See you on the other side.

*— Vets Who Code*

---

**Questions?** hello@vetswhocode.io

**[vetswhocode.io](https://vetswhocode.io)**

</div>
