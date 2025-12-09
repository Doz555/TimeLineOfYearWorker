# Contributing to Timeline of Year

Thank you for your interest in contributing to the Timeline of Year project! This document provides guidelines and instructions for contributing.

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)
- [Pull Request Process](#pull-request-process)
- [Development Guidelines](#development-guidelines)
- [Commit Messages](#commit-messages)

---

## Code of Conduct

### Our Pledge
We are committed to providing a welcoming and inspiring community for all. Please be respectful and constructive in all interactions.

### Expected Behavior
- Use welcoming and inclusive language
- Be respectful of differing opinions
- Provide and accept constructive criticism
- Focus on what is best for the community
- Show empathy towards other community members

### Unacceptable Behavior
- Harassment or discrimination of any kind
- Insulting or derogatory comments
- Trolling or inflammatory comments
- Publishing others' private information
- Other conduct which could be considered inappropriate

---

## Getting Started

### Prerequisites
- Git installed on your computer
- A GitHub account
- A text editor or IDE (VS Code recommended)
- Basic understanding of HTML, CSS, and JavaScript

### Setup Development Environment

1. **Fork the Repository**
   - Click the "Fork" button on GitHub
   - Clone your fork to your local machine:
   ```bash
   git clone https://github.com/YOUR_USERNAME/TimeLineOfYear.git
   cd TimeLineOfYear
   ```

2. **Create a Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
   or
   ```bash
   git checkout -b fix/your-bug-fix
   ```

3. **Make Your Changes**
   - Edit files as needed
   - Test your changes in a web browser
   - Verify all functionality works

4. **Test Your Changes**
   - Open the HTML files in multiple browsers
   - Test on different screen sizes (desktop, tablet, mobile)
   - Check that CSV data loads correctly

---

## How to Contribute

### Types of Contributions

#### 🐛 Bug Reports
- Report issues you find with the application
- Provide clear reproduction steps
- Include browser and OS information
- Attach screenshots if applicable

#### 📝 Documentation
- Improve existing documentation
- Add clarifications or examples
- Fix typos and errors
- Create guides for common tasks

#### ✨ Features
- Suggest new features or enhancements
- Propose improvements to existing features
- Share ideas for better UX/UI

#### 🎨 Code Improvements
- Refactor code for clarity
- Optimize performance
- Improve code organization
- Add comments and documentation

#### 🌐 Localization
- Help translate documentation
- Add support for new languages
- Improve Thai language content

---

## Reporting Bugs

### Before Submitting a Bug Report
- Check if the issue already exists
- Try the latest version of the code
- Clear your browser cache
- Test in different browsers
- Review the troubleshooting guide

### How to Submit a Bug Report

Create an issue with the following information:

```
Title: Brief description of the bug

Environment:
- Browser: [e.g., Chrome 120, Firefox 121]
- OS: [e.g., Windows 10, macOS 14]
- Screen Size: [e.g., 1920x1080, mobile]

Description:
Detailed description of the issue

Reproduction Steps:
1. Step one
2. Step two
3. ...

Expected Behavior:
What should happen

Actual Behavior:
What actually happens

Screenshots:
[Attach screenshots if helpful]

Additional Context:
Any other relevant information
```

---

## Suggesting Enhancements

### Before Submitting a Suggestion
- Check if the feature already exists
- Review existing issues for similar suggestions
- Consider if the feature aligns with project goals

### How to Submit a Suggestion

Create an issue with the following:

```
Title: [FEATURE REQUEST] Brief description

Description:
Detailed explanation of the feature

Use Case:
Why would this feature be useful?

Example:
How would this feature work?

Alternatives:
Other ways to solve this problem

Additional Context:
Any other relevant information
```

---

## Pull Request Process

### Before Submitting a PR
1. Ensure your code follows project standards
2. Test all changes thoroughly
3. Update documentation if needed
4. Create clear commit messages
5. Sync with the latest upstream changes

### Submitting a Pull Request

1. **Push to Your Fork**
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Create Pull Request**
   - Go to your fork on GitHub
   - Click "Compare & pull request"
   - Fill in the PR template:

```
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Code refactoring

## Related Issues
Fixes #[issue number]

## Changes Made
- Change 1
- Change 2
- Change 3

## Testing
Describe how you tested changes:
- [ ] Tested in Chrome
- [ ] Tested in Firefox
- [ ] Tested on mobile
- [ ] Tested CSV loading
- [ ] Tested data parsing

## Screenshots (if applicable)
[Add screenshots here]

## Checklist
- [ ] Code follows style guidelines
- [ ] Documentation updated
- [ ] No new warnings generated
- [ ] Changes tested
- [ ] Commits have clear messages
```

### PR Review Process
1. Maintainers will review your PR
2. Changes may be requested
3. Once approved, PR will be merged
4. Your contribution is credited

---

## Development Guidelines

### Code Style

#### HTML
- Use semantic HTML5 elements
- Proper indentation (2 spaces)
- Meaningful class and id names
- Keep structure clean and organized

```html
<div class="timeline-container">
    <div class="timeline-item dept-it">
        <div class="timeline-content">
            <h3>Project Name</h3>
            <p>2025/01/01 - 2025/01/05</p>
        </div>
    </div>
</div>
```

#### CSS
- Use CSS custom properties for colors
- Group related styles together
- Comment complex selectors
- Mobile-first approach

```css
:root {
    --primary: #4361ee;
    --success: #06d6a0;
}

.timeline-item {
    padding: 1rem;
    border-left: 5px solid var(--primary);
}

/* Mobile styles */
@media (max-width: 768px) {
    .timeline-item {
        width: 100%;
    }
}
```

#### JavaScript
- Use meaningful variable and function names
- Add comments for complex logic
- Follow DRY (Don't Repeat Yourself) principle
- Optimize performance

```javascript
// Load and parse CSV data
function loadTimelineData(filePath) {
    return fetch(filePath)
        .then(response => response.text())
        .then(data => parseCSV(data))
        .catch(error => console.error('Error loading data:', error));
}

// Parse CSV content into array of objects
function parseCSV(csvText) {
    const [header, ...rows] = csvText.split('\n');
    const headers = header.split(',');
    
    return rows
        .filter(row => row.trim())
        .map(row => {
            const values = row.split(',');
            return Object.fromEntries(
                headers.map((h, i) => [h.trim(), values[i]?.trim()])
            );
        });
}
```

### Naming Conventions

- **Classes**: `kebab-case` (e.g., `timeline-item`, `dept-it`)
- **IDs**: `camelCase` (e.g., `timelineContainer`)
- **Variables**: `camelCase` (e.g., `projectData`, `startDate`)
- **Functions**: `camelCase` (e.g., `loadData()`, `renderTimeline()`)
- **Constants**: `UPPER_SNAKE_CASE` (e.g., `MAX_ITEMS`, `DATE_FORMAT`)

### Comments

- Write clear, concise comments
- Explain WHY, not WHAT
- Keep comments up-to-date with code

```javascript
// Good comment
// Use flex layout for responsive timeline items
.timeline-item {
    display: flex;
    flex-wrap: wrap;
}

// Avoid obvious comments
// Set display to flex
.timeline-item {
    display: flex;
}
```

---

## Commit Messages

### Format
```
[TYPE] Brief summary (50 chars or less)

Detailed explanation of changes (if needed)
Wrapped at 72 characters

Fixes #issue_number (if applicable)
```

### Types
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation change
- `style`: Code style change (no logic change)
- `refactor`: Code refactoring
- `perf`: Performance improvement
- `test`: Add or update tests
- `chore`: Build process, dependencies, etc.

### Examples

**Good commit messages:**
```
feat: Add dark mode toggle to timeline

Implement a theme switcher that allows users to toggle between light and dark mode.
Persists user preference in localStorage.

docs: Update CSV format in README

Clarify the date format requirement (YYYY/MM/DD) with examples.

fix: Correct department color for HT_Report

Change HT_Report color from #7209b7 to match design specification.
Fixes #42
```

**Avoid:**
```
❌ "update"
❌ "fixed stuff"
❌ "changes"
❌ "asdf"
```

---

## Testing Guidelines

### Manual Testing Checklist

- [ ] HTML renders correctly
- [ ] CSS styles apply properly
- [ ] JavaScript code executes without errors
- [ ] CSV data loads and displays
- [ ] All departments show correct colors
- [ ] Dates parse correctly
- [ ] Text displays in Thai without issues
- [ ] Responsive design works on all sizes
- [ ] Works in Chrome, Firefox, Safari, Edge
- [ ] No console errors or warnings

### Browser Testing

Test your changes in:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (if applicable)

### Performance Testing

- Check page load time
- Verify no unnecessary network requests
- Monitor memory usage
- Test with large datasets (100+ records)

---

## Documentation Updates

When contributing, please update relevant documentation:

- **README.md** - For major features or breaking changes
- **DOCUMENTATION.md** - For technical details
- **USAGE.md** - For user-facing changes
- **Code comments** - For implementation details

---

## Project Structure Guidelines

Keep the project organized:
```
TimeLineOfYear/
├── *.html              # Main timeline views
├── data.csv            # Timeline data
├── README.md           # Project overview
├── DOCUMENTATION.md    # Technical docs
├── USAGE.md            # User guide
├── CONTRIBUTING.md     # This file
└── LICENSE             # License file
```

---

## Questions?

- Check existing issues and discussions
- Review documentation thoroughly
- Ask in a new issue before starting major work
- Be patient - maintainers volunteer their time

---

## Recognition

Contributors will be recognized in:
- Project README
- Release notes
- Git commit history

---

## License

By contributing, you agree that your contributions will be licensed under the same license as the project.

---

## Additional Resources

- [GitHub Help](https://help.github.com/)
- [Git Documentation](https://git-scm.com/doc)
- [HTML5 Specification](https://html.spec.whatwg.org/)
- [CSS Tricks](https://css-tricks.com/)
- [MDN Web Docs](https://developer.mozilla.org/)

---

Thank you for contributing to Timeline of Year! 🎉

Together, we make this project better for everyone.
