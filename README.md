# Clear Authz CLI Tool

## Problem

Sometimes, the authz requests sending to LetsEncrypt may be _bad_. This leads
to authz request hanging in the "pending" status; and causing the request sending
to the LetsEncrypt to fail because of "rate-limit".

## Solution

This quick CLI option enable the option to clear out the authz requests sending
stuck on LetsEncrypt API.

## Usage

`cat /var/log/letsencrypt/* | ./clear-authz /path/to/private_key.json`

After running the command above, you should be able to clear out the "pending"
authz request using LetsEncrypt API
