# markdown-content

This repository contains the user facing documentation that populates app.stateless.solutions/documentation.

## Current Navigation

```bash
export const navItems = [
  {
    sortOrder: 0,
    route: '',
    label: 'Get Started',
  },
  {
    sortOrder: 1,
    route: '/documentation/get-started/overview',
    label: 'Overview',
  },
  {
    sortOrder: 2,
    route: '/documentation/get-started/basic-concepts’,
    label: 'Overview',
  },
  {
    sortOrder: 3,
    route: '/documentation/get-started/application-quickstart',
    label: 'Application Quickstart',
  },
  {
    sortOrder: 4,
    route: '/documentation/user-guides',
    label: 'Provider Quickstart',
  },
  {
    sortOrder: 5,
    route: '/documentation/user-guides/application-guides',
    label: 'User Guides',
  },
  {
    sortOrder: 6,
    route: '/documentation/user-guides/application-guides/managing-api-keys',
    label: 'Application Guides',
  },
  {
    sortOrder: 7,
    route: '/documentation/user-guides/application-guides/selecting-service-providers',
    label: 'Managing API Keys',
  },
  {
    sortOrder: 8,
    route: '/documentation/user-guides/provider-guides',
    label: 'Provider Guides',
  },
  {
    sortOrder: 9,
    route: '/documentation/user-guides/provider-guides/provider-onboarding',
    label: 'Provider Onboarding',
  },
  {
    sortOrder: 10,
    route: '/documentation/user-guides/provider-guides/service-expectations-responsibilities',
    label: 'Service Expectations and Responsibilities',
  },
];
```
## Expected Format

```bash
// Route should be empty string or null for headers
// Name in contentData should match value after last "/"

export const navItems = [
  {
    sortOrder: 0,
    route: '',
    label: 'Get Started',
  },
  {
    sortOrder: 1,
    route: '/documentation/overview',
    label: 'Overview',
  },
  {
    sortOrder: 2,
    route: '/documentation/application-quickstart',
    label: 'Application Quickstart',
  },
  {
    sortOrder: 3,
    route: '/documentation/provider-quickstart',
    label: 'Provider Quickstart',
  },
  {
    sortOrder: 4,
    route: '',
    label: 'User Guides',
  },
  {
    sortOrder: 5,
    route: '/documentation/applications',
    label: 'Applications',
  },
  {
    sortOrder: 6,
    route: '/documentation/providers',
    label: 'Providers',
  },
  {
    sortOrder: 7,
    route: '',
    label: 'Developer Reference',
  },
  {
    sortOrder: 8,
    route: '/documentation/cli',
    label: 'CLI',
  },
  {
    sortOrder: 9,
    route: '/documentation/python-sdk',
    label: 'Python SDK',
  },
  {
    sortOrder: 10,
    route: '/documentation/javascript-sdk',
    label: 'Javascript SDK',
  },
];

export const contentData = [
  {
    name: 'overview',
    content:
      '# Overview\n\nLorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat..\n\n ## Getting Started \n\n - Lorem ipsum dolor sit amet \n\n - Lorem ipsum dolor sit amet \n\n - Lorem ipsum dolor sit amet \n\n - Lorem ipsum dolor sit amet \n\n - Lorem ipsum dolor sit amet \n\n - Lorem ipsum dolor sit amet \n\n# Key Concepts\n\n## API Middleware\n\nLorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
  },
  {
    name: 'application-quickstart',
    content:
      '# Application Quickstart\n\nHere, you will find all the details needed to quickly get started with applications.',
  },
  {
    name: 'provider-quickstart',
    content:
      '# Provider Quickstart\n\nThis section covers all you need to know about starting with providers.',
  },
  {
    name: 'applications',
    content: '# Applications\n\nDetailed user guide for applications.',
  },
  {
    name: 'providers',
    content: '# Providers\n\nLearn more about how providers work in our system.',
  },
  {
    name: 'cli',
    content: '# CLI\n\nCommand Line Interface (CLI) details and reference.',
  },
  {
    name: 'python-sdk',
    content: '# Python SDK\n\nA guide and reference for the Python Software Development Kit.',
  },
  {
    name: 'javascript-sdk',
    content:
      '# Javascript SDK\n\nHere you can find more about the Javascript SDK, its methods, and examples.',
  },
];
```
