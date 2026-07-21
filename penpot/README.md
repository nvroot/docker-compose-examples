

Secret key#
The PENPOT_SECRET_KEY envvar serves a master key from which other keys for subsystems (eg http sessions, or invitations) are derived.

To use it, we recommend using a truly randomly generated 512 bits base64 encoded string here. You can generate one with:
```
python3 -c "import secrets; print(secrets.token_urlsafe(64))"
```
And configure it:
# Backend
PENPOT_SECRET_KEY: my-super-secure-key