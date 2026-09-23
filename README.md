# adapt-seo-articles
# Adapt SEO Articles

Turn an original SEO or GEO article into a publication-ready draft for **DigiKey TechForum, Medium, LinkedIn newsletters, or IoT For All**.

This skill checks factual claims, removes repetitive or overly promotional language, and rewrites the article for the readers and editorial expectations of each platform. It also places a relevant link to your own website or landing page in the article body.

## Download and install

Download [adapt-seo-articles.zip](./adapt-seo-articles.zip) from this repository. The ZIP should contain the `adapt-seo-articles` folder, with `SKILL.md` inside it.

### ChatGPT

1. Open **Plugins → Skills**.
2. Select **Create → Upload from your computer**.
3. Upload `adapt-seo-articles.zip`.
4. Once the skill is available, mention it in your request or ask ChatGPT to adapt an article for one of the supported platforms.

Skill availability depends on your ChatGPT account and workspace settings.

### Claude

1. Open **Customize → Skills**.
2. Select **+ → Create skill → Upload a skill**.
3. Upload `adapt-seo-articles.zip` and enable the skill.

You can also use the `SKILL.md` folder with other agents that support the Agent Skills format. Follow that platform’s installation instructions.

## What to provide

For each article, provide:

* The original article text, document, or URL
* The target platform or platforms
* **Your own website or landing-page URL** to include in the guest article
* Any important requirements, such as audience, product focus, or claims that need checking

The original article URL and the landing-page URL serve different purposes. Provide both when they are available.

**Example request:**

> Use Adapt SEO Articles to revise this article for LinkedIn newsletters and Medium: [article URL]. My landing page is [your URL]. Keep the technical conclusions, check factual claims, and include the landing-page link naturally in each article body.

## What you receive

For each requested platform, the skill produces a separate draft with:

* A platform-appropriate title and complete article
* A relevant landing-page link within the article body
* Available publishing metadata, such as a LinkedIn SEO title and description
* A short list of claims or submission details that still need verification
* A brief explanation of what was changed

If an article or link does not fit a platform’s rules, the skill flags the issue and suggests a workable angle. **It prepares drafts; it does not submit or publish them automatically.** IoT For All submissions remain subject to editorial review.

## Seeed Studio examples

For articles authored by Seeed Studio, the skill can select a relevan
