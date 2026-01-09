### Scope 
```text
mp-comm-retail-api/
├── .github/
│   ├── PULL_REQUEST_TEMPLATE/
│   │   ├── feature.md
│   │   └── fix.md
```

---

### Bug
`/swagger` endpoint was returning 500

---

### Fix
Exempted `/swagger` endpoint

---

### Endpoints
#### Purchase Endpoints
**URI:** `base/po/list`

**Query Parameters:** [`page_nr`, `limit`]

**Request Body:**
```python
{
	'filters': {
		'po_type': 'retail_rtv' # other valid values = ['retail_adhoc', ...]
	}
}
```

**Response Body:**
```python
{
	'po_nr': 'POGC4535729AE'
	# ...
}
```

---

### Suggested Order of Viewing
1. `apppurchase/web.py`
