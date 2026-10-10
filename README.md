# Birthday Surprise Website

This project is a static birthday page that works directly on GitHub Pages without any build step or backend.

## Usage

The website reads the personal data only from URL query parameters. No personal information is stored in the repository.

Example:

```text
https://weinchris.github.io/birthday-app/?name=Anna&birthdate=1998-10-04T14:30:00+02:00&theme=rose
```

This will display:

- `name` = the person's name
- `birthdate` = the birth date and time
- `theme` = optional visual style (`midnight`, `rose`, `champagne`, `forest`)

The page supports ISO-8601 values, including timezones. A value with an explicit timezone is the most reliable option:

```text
?name=Anna%20Maria&birthdate=1998-10-04T14:30:00%2B02:00&theme=rose
```

This is equivalent to:

```text
?name=Anna Maria&birthdate=1998-10-04T14:30:00+02:00&theme=rose
```

### Important privacy note

Personal data is not saved in the repository. The site reads everything from the URL at runtime only. It does not use cookies, local storage, analytics, or tracking.

### Fallback behavior

- If no `name` parameter exists, the page shows: `Dear You ❤️`
- If no `birthdate` parameter exists, the page shows a friendly message asking for the birthday date.
- If the date is invalid, the page shows a friendly error instead of failing.
- If no `theme` parameter exists, the page uses the default luxury palette.

## Notes

- The site uses plain HTML5, CSS3, and vanilla JavaScript.
- It is intentionally static and can be hosted on GitHub Pages with no build tools.
- No external asset or library is required.

## Example URLs

```text
https://weinchris.github.io/birthday-app/?name=Anna&birthdate=1998-10-04T14:30:00+02:00&theme=midnight
https://weinchris.github.io/birthday-app/?name=Anna%20Maria&birthdate=1998-10-04T14:30:00%2B02:00&theme=rose
https://weinchris.github.io/birthday-app/?name=Alex&birthdate=2001-12-25T09:15:00Z&theme=champagne
```
