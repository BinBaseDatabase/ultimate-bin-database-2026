# Implementation Guide for Multi-Length BIN Lookup

To get 100% accuracy with our 3.5M+ database, use the following logic to handle 6, 8, 9, 10, and 11-digit BINs.

### 🐍 Python Example
```python
def get_card_details(pan, database_dict):
    # Take up to 11 digits
    search_prefix = str(pan)[:11]
    
    # Waterfall lookup: 11 -> 10 -> 9 -> 8 -> 6
    for length in [11, 10, 9, 8, 6]:
        bin_candidate = search_prefix[:length]
        if bin_candidate in database_dict:
            return database_dict[bin_candidate]
    return None

function lookupBin($pan, $db) {
    $cleanPan = substr(preg_replace('/\D/', '', $pan), 0, 11);
    $lengths = [11, 10, 9, 8, 6];

    foreach ($lengths as $l) {
        $prefix = substr($cleanPan, 0, $l);
        if (isset($db[$prefix])) {
            return $db[$prefix];
        }
    }
    return null;
}

-- The most efficient way to query indexed BIN table
SELECT * FROM bin_table 
WHERE bin IN ('46712250211', '4671225021', '467122502', '46712250', '467122')
ORDER BY LENGTH(bin) DESC
LIMIT 1;
