codeigniter-oracle
==================

# Make codeigniter work with Oracle 10g db

I will be adding code here and (blog it here)[http://sourcehut.tumblr.com/post/68429547352/convert-codeigniter-from-mysql-to-oracle]

Though in theory it should be as simple as it's in Rails but looks like that Oracle support in codeigniter is an after thought and no one actually uses it.

## Here is the list of the issues that came up and had to be solved.

- Oracle needs that field names in generated SQL’s be ‘single-quoted’, where as MySQL can work without the Quotes.
- DateTimes handling id very different between MySQL & Oracle.
- Oracle returns records set with CAPITAL field NAMES.
- There is no auto increment index field in Oracle, which is commonly used in ID field in MySQL for CodeIgniter
- There is no straight way to get the LAST INSERTED ID in Oracle.
- LIMIT as needed for paging is not implemented in CodeIgniter Oracle driver.
- Double quotes generated by CodeIgniter in WHERE clause crash.