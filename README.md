# Creating Documentation in the Ape Ecosystem

If you're working on a project within the Ape ecosystem follow the steps below, they will set you up with a standard ape template for documentation and deploy them in a [GitHub Pages](https://pages.github.com/) for your repo.

Any repo configured with GitHub Pages within the ApeWorX organization will be published automatically at `https://docs.apeworx.io/your_repo_name_here`.

## Quick Start

1. **Set Up Repository:**
   - Create a new repo under the ApeWorX organization if one doesn’t exist for your project.

2. **Copy Necessary Files and Folders:**
   - Copy the `./docs` folder from this reference repo to your repo.
   - Copy the `./build_docs.py` file from this reference repo to your repo.
   - Copy the `.github/workflows/docs.yaml` file from this reference repo to your repo.
   - Edit lines 35 and 43 from `.github/workflows/docs.yaml` with your repo name

3. **Write User Guides and Method Docs:**
   - Add new user guides to `./docs/userguides`. The sidebar will be autogenerated and display each guide's first title.
   - Edit `docs/index.md` to adjust the sidebar table-of-content.
   - To generate documentation from docstrings in your code, use `./docs/methoddocs` and adhere to the provided [syntax guide](#Syntax-Guide-for-Python-Sphinx).

4. **Generate and Publish Documentation:**
   - Run the `./build_docs.py` script to generate the documentation.
   - Push your changes to the repo. Your documentation will be automatically published to `https://docs.apeworx.io/repo_name_here`.

## Features:

- **Autogenerated Sidebar:** The sidebar is autogenerated for all user guides and methods and will display the first title from each user guide. Ensure the first title accurately represents the content of the guide.
- **Repo README is the default landing page:** Your repo `README.md` file will automatically become a user guide titled “Quickstart”.

## Best Practices:

- **Keep Documentation Updated:** Regularly update the documentation to reflect changes and updates in the project.
- **Be Clear and Concise:** Write documentation that is clear, concise, and easy to understand for all team members. Remember that most readers have less context about what you are documenting.
- **Use Descriptive Titles:** The first title in your user guides will be displayed in the autogenerated sidebar, so ensure it is descriptive and accurately represents the guide's content.

By following these guidelines, you will ensure that the documentation for your project is consistent, user-friendly, and easily accessible to all team members within the Ape ecosystem.


## Syntax Guide for Python Sphinx

To document Python modules using Sphinx, you can use the `.. automodule::` directive like this:

```rst
.. automodule:: silverback.application
    :members:
    :show-inheritance:
```
