# Repository Clone Tracking Setup Guide

## Overview
This guide explains how the clone count tracking feature works in this GitHub profile README and how to enable it.

## Features Implemented

### 1. GitHub Traffic API Badges
The README now includes badges that display:
- **Total Clones (14 days)**: Shows the total number of times the repository has been cloned in the last 14 days
- **Unique Clones (14 days)**: Shows the number of unique users who cloned the repository in the last 14 days

### 2. Badge Types Added

#### In the Header Section:
```markdown
![GitHub Clones](https://img.shields.io/badge/dynamic/json?color=success&label=Clone&query=count&url=https://gist.githubusercontent.com/maxvyquincy9393/clone-stats/raw/clone.json&logo=github&style=for-the-badge)
![GitHub Visitors](https://img.shields.io/badge/dynamic/json?color=informational&label=Visitors&query=count&url=https://gist.githubusercontent.com/maxvyquincy9393/visitor-stats/raw/visitor.json&logo=github&style=for-the-badge)
```

#### In the Repository Traffic Section:
```markdown
![GitHub Clones (14 days)](https://img.shields.io/github/clones/maxvyquincy9393/maxvyquincy9393?style=for-the-badge&label=Clones%20(14%20days)&color=blue)
![GitHub Unique Clones (14 days)](https://img.shields.io/github/clones/maxvyquincy9393/maxvyquincy9393/unique?style=for-the-badge&label=Unique%20Clones&color=brightgreen)
```

## How It Works

### GitHub Traffic API
GitHub provides traffic data through its API, which includes:
- Clone counts (total and unique)
- View counts
- Referrer information
- Popular content

The badges use shields.io service to fetch and display this data dynamically.

### Important Notes

1. **14-Day Window**: GitHub's traffic API only stores data for the last 14 days. This is a GitHub limitation, not a limitation of the badges.

2. **Authentication**: The badges that use GitHub's traffic API require the repository owner to be authenticated. For public repositories, the data may be visible to all users.

3. **Update Frequency**: The badges update dynamically, but there may be a caching delay (usually a few minutes).

## Setup Requirements

### For the Dynamic JSON Badges (Optional)
If you want to use the dynamic JSON badges in the header, you'll need to:

1. Create a GitHub Gist to store traffic statistics
2. Set up a GitHub Action to periodically fetch and update the statistics
3. Update the badge URLs to point to your gist

### For the GitHub Traffic API Badges (Already Working)
These badges are already functional and will display clone statistics for:
- Repository: `maxvyquincy9393/maxvyquincy9393`
- Data: Last 14 days of clone activity

## Customization

### Changing Badge Style
You can customize the badge appearance by modifying the `style` parameter:
- `style=for-the-badge` (current style)
- `style=flat-square`
- `style=flat`
- `style=plastic`
- `style=social`

### Changing Badge Colors
Modify the `color` parameter:
- `color=blue`
- `color=brightgreen`
- `color=success`
- `color=informational`
- `color=red`
- Or use hex colors: `color=ff69b4`

## Troubleshooting

### Badges Not Displaying
1. Check if the repository is public
2. Verify the username and repository name in the badge URLs
3. Check GitHub's status page for API issues
4. Clear browser cache

### No Data Showing
1. Clone statistics only show data from the last 14 days
2. New repositories may not have clone data yet
3. Private repositories may require authentication

## Additional Resources

- [GitHub Traffic API Documentation](https://docs.github.com/en/rest/metrics/traffic)
- [Shields.io Documentation](https://shields.io/)
- [GitHub Profile README Guide](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)

## Future Enhancements

Consider implementing:
1. Historical clone tracking beyond 14 days using GitHub Actions
2. Clone trend graphs
3. Integration with analytics platforms
4. Export functionality for clone statistics

---

**Created**: 2026-02-07  
**Repository**: maxvyquincy9393/maxvyquincy9393
