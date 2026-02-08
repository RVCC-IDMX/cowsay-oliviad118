# Getting Started with npm

This tutorial walks you through creating your first npm project and installing your first package. We'll use the fun `cowsay` package as our example!

## What is npm?

npm stands for "Node Package Manager." Think of it like an app store for JavaScript code. Developers share useful code as "packages" that you can easily add to your projects.

**Why use npm?**
- Saves time by reusing existing code
- Automatically handles dependencies (packages that depend on other packages)
- Keeps track of what packages your project uses

## Step 1: Initialize Your Project

Before you can install packages, you need to create a `package.json` file. This file is like a recipe card for your project - it lists all the "ingredients" (packages) your project needs.

```bash
npm init -y
```

### What this command does:

- `npm init` - Creates a new package.json file
- `-y` - Says "yes" to all the default options (faster setup)

**Example output:**
```json
{
  "name": "cowsay-oliviad118",
  "version": "1.0.0",
  "description": "Welcome to Week 2! This assignment teaches you to use Copilot Agent for project setup while you learn npm basics through the fun cowsay package.",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
```

## Step 2: Install Your First Package

Now let's install the `cowsay` package, which creates ASCII art of a cow saying whatever message you give it.

```bash
npm install cowsay
```

### What this command does:

- Downloads the cowsay package and all its dependencies
- Creates a `node_modules` folder to store the code
- Adds cowsay to your package.json dependencies
- Creates a `package-lock.json` file to lock specific versions

**What you'll see:**
```
added 41 packages, and audited 42 packages in 1s

3 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

### Don't worry about these messages:

- **"41 packages"** - cowsay needs other packages to work, so npm installed those too
- **"looking for funding"** - Just a notice that some package authors accept donations (not an error!)
- **"0 vulnerabilities"** - Good news! No security issues found

## Step 3: Test Your Installation

Use `npx` to run the cowsay package without installing it globally:

```bash
npx cowsay Hello
```

### What `npx` means:

- **npm** = manages packages (install, update, remove)  
- **npx** = executes packages (runs them right now)

**Expected output:**
```
 _______
< Hello >
 -------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

## What You've Created

After following these steps, your project will have:

### Files created:
- **package.json** - Your project configuration and dependency list
- **package-lock.json** - Locks specific versions for consistent installs
- **node_modules/** - Folder containing all installed packages (don't edit this!)

### Updated package.json:
Your package.json now includes a `dependencies` section:
```json
"dependencies": {
  "cowsay": "^1.6.0"
}
```

## Next Steps

Now that you have npm set up and your first package installed, you can:

1. Try different cowsay commands (see creature options)
2. Learn about npm scripts to automate common tasks
3. Explore other fun packages on [npmjs.com](https://www.npmjs.com)

## Troubleshooting

**Terminal shows weird characters?** 
- Try using single quotes instead of double quotes around your message
- Or skip quotes entirely for single words: `npx cowsay Hello`

**Command not found?**
- Make sure you're in the right folder (where your package.json is)
- Check that the installation completed successfully

---

*This tutorial assumes you have Node.js and npm already installed on your computer.*