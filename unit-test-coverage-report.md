# Unit Test Coverage Static Analysis Report

Repository: `djangoproject.com`

Method: static, language-agnostic file-ratio analysis (no tests executed, no source modified).

## Summary

| Metric | Value |
| --- | --- |
| Estimated coverage (source files with a matching test file) | **32.0%** |
| Total source files analyzed | 153 |
| Source files with corresponding test files | 49 |
| Source files missing test files | 104 |
| Test files discovered | 36 |
| Threshold | 80% |

Consistency check: 49 covered + 104 uncovered = 153 total source files.

## Finding

**Estimated unit test coverage is 32.0%, which is below the 80% threshold.** 104 of 153 source files have no corresponding test file. The uncovered files are listed below, grouped by directory.

## Files Missing Tests

### `_sphinx_13448_workaround/` (2 files)

- `__init__.py`
- `apps.py`

### `accounts/` (2 files)

- `__init__.py`
- `urls.py`

### `aggregator/` (4 files)

- `__init__.py`
- `context_processors.py`
- `feeds.py`
- `urls.py`

### `aggregator/management/` (1 files)

- `__init__.py`

### `aggregator/management/commands/` (3 files)

- `__init__.py`
- `send_pending_approval_email.py`
- `update_subscriptions.py`

### `blog/` (4 files)

- `__init__.py`
- `feeds.py`
- `sitemaps.py`
- `urls.py`

### `blog/templatetags/` (2 files)

- `__init__.py`
- `weblog.py`

### `checklists/` (3 files)

- `__init__.py`
- `apps.py`
- `urls.py`

### `checklists/templatetags/` (2 files)

- `__init__.py`
- `checklist_extras.py`

### `contact/` (2 files)

- `__init__.py`
- `urls.py`

### `dashboard/` (2 files)

- `__init__.py`
- `urls.py`

### `dashboard/management/` (1 files)

- `__init__.py`

### `dashboard/management/commands/` (3 files)

- `__init__.py`
- `fix_trac_metrics.py`
- `update_metrics.py`

### `djangoproject/` (5 files)

- `__init__.py`
- `hosts.py`
- `middleware.py`
- `sitemaps.py`
- `thumbnails.py`

### `djangoproject/settings/` (5 files)

- `__init__.py`
- `common.py`
- `dev.py`
- `docker.py`
- `prod.py`

### `djangoproject/static/js/` (4 files)

- `admin_blog_imageupload.js`
- `djangoproject.js`
- `fundraising-heart.js`
- `main.js`

### `djangoproject/static/js/dashboard/` (2 files)

- `detail.js`
- `index.js`

### `djangoproject/static/js/mod/` (4 files)

- `list-collapsing.js`
- `stripe-change-card.js`
- `stripe-donation.js`
- `switch-dark-mode.js`

### `djangoproject/urls/` (2 files)

- `__init__.py`
- `docs.py`

### `docs/` (7 files)

- `__init__.py`
- `apps.py`
- `context_processors.py`
- `search.py`
- `sitemaps.py`
- `urls.py`
- `views_debug.py`

### `docs/management/` (1 files)

- `__init__.py`

### `docs/management/commands/` (3 files)

- `__init__.py`
- `purge_docs_cache.py`
- `update_docs.py`

### `docs/templatetags/` (2 files)

- `__init__.py`
- `docs.py`

### `foundation/` (2 files)

- `__init__.py`
- `feeds.py`

### `foundation/templatetags/` (3 files)

- `__init__.py`
- `banner.py`
- `meetings.py`

### `foundation/urls/` (2 files)

- `__init__.py`
- `meetings.py`

### `fundraising/` (5 files)

- `__init__.py`
- `admin_views.py`
- `apps.py`
- `exceptions.py`
- `urls.py`

### `fundraising/management/commands/` (1 files)

- `create_stripe_plans.py`

### `fundraising/templatetags/` (2 files)

- `__init__.py`
- `fundraising_extras.py`

### `legacy/` (2 files)

- `__init__.py`
- `urls.py`

### `members/` (2 files)

- `__init__.py`
- `urls.py`

### `members/management/commands/` (1 files)

- `send_renewal_emails.py`

### `releases/` (3 files)

- `__init__.py`
- `context_processors.py`
- `urls.py`

### `releases/management/` (1 files)

- `__init__.py`

### `releases/management/commands/` (2 files)

- `__init__.py`
- `generate_release_roadmap.py`

### `releases/templatetags/` (3 files)

- `__init__.py`
- `date_format.py`
- `release_notes.py`

### `svntogit/` (3 files)

- `__init__.py`
- `mapping.py`
- `urls.py`

### `tracdb/` (6 files)

- `__init__.py`
- `db_router.py`
- `stats.py`
- `testutils.py`
- `tractime.py`
- `urls.py`

## Unmatched Test Files

These test files correspond to no single source file (shared fixtures, cross-cutting/integration suites, or package-level test modules). They are excluded from the covered-source count so the coverage numerator reflects covered sources only.

- `accounts/tests.py`
- `aggregator/tests.py`
- `blog/tests.py`
- `checklists/tests/__init__.py`
- `checklists/tests/factory.py`
- `checklists/tests/test_templatetags.py`
- `contact/tests.py`
- `dashboard/tests.py`
- `djangoproject/test_registration.py`
- `djangoproject/tests.py`
- `djangoproject/tests/test_www_urls.py`
- `docs/tests/__init__.py`
- `docs/tests/test_templates.py`
- `foundation/tests.py`
- `fundraising/tests/__init__.py`
- `fundraising/tests/test_templatetags.py`
- `legacy/tests.py`
- `members/test_management.py`
- `releases/tests.py`
- `svntogit/tests.py`
- `tracdb/tests.py`

## Recommendation

The project is below the 80% unit test coverage threshold at 32.0%. Add unit tests for the 104 source files listed under "Files Missing Tests", prioritizing modules that contain business logic (views, models, forms, management commands, and utility modules) over thin configuration or declaration-only modules. Note that this is a structural estimate based on file naming and layout; it does not measure executed line coverage. Django projects commonly place all tests for an app in a single `tests.py` or `tests/` package, so some listed files may in fact be exercised indirectly by an app-level test module.

