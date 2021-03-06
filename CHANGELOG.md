## 3.0.1

### Bug Fixes

- Fix an issue where builds may produce styles in an unpredictable order.
- Fix an issue where `.usa-display` heading font size was rendered larger than intended.
- Fix an issue where `dropdownButton` was using invalid CommonJS syntax when imported from ES module entrypoint.

### Internal

- Replace deprecated USWDS variable references with updated equivalent values.

## 3.0.0

### Breaking Changes

- Updates USWDS from 2.0.3 to 2.9.0. Review [release notes](https://designsystem.digital.gov/about/releases/) for specific changes which may apply. Specific impactful changes include...
  - The Tooltip component is now inherited from USWDS, newly introduced as of USWDS 2.8.0. [See component documentation](https://designsystem.digital.gov/components/tooltip/) for more information. The markup of this component is significantly different than that of the component previously implemented in the login.gov Design System.
  - Due to a rounding precision fix, line-heights for text may appear larger than it had previously.
  - Guidance for many components has been updated to improve accessibility and usability of markup. Neglecting to update this markup should not result in user-facing regressions, but you are recommended to update to improve end-user experience. Refer to the release notes and related component documentation for specifics:
    - SVG images should include `role="img"`.
    - Numeric fields should use `type="text" inputmode="numeric"` instead of `type="number"`.
    - Search forms should assign `role="search"` to the form element.
    - Banner should be rendered as a `section` element instead of a `div`, and include a descriptive `aria-label`.
    - Footer and hero content should include a descriptive `aria-label`.
    - Graphic list should use `h2` as a heading element instead of `h3`.
- "Official government website" banner text has been updated. Refer to [USWDS guidance](https://designsystem.digital.gov/components/banner/) for updated markup.

### New Features

- The published NPM package can now be imported into a project. Bundlers that support dead-code elimination (Webpack, etc.) can automatically remove unused code to optimize bundle size. See [Usage guide](https://design.login.gov/usage/) for more information. Existing usage of JavaScript code from `dist/assets/` is unaffected by these changes.

### Bug Fixes

- Fixed support for multiple dropdown buttons on a page.
