# Input

> vf-input


- [Introduction](#introduction)
- [Props](#prop)
- [Methods](#methods)
- [Events](#server-side)
- [Salesforce config](#salesforce-config)


# Introduction
The `vf-input` component allows devlopers to quickly generate input forms without the hassle of struggling with describe information.

Cuerrntly **there are not supported** the following Salesforce field types:

* Rich text


## Props

### value [Object]
The model

### field [String]

The full-name of the Salesforce field. For example `Account.Name`. If it uses a namespace make sure to include it `pkgnamespace__Object.pkgnamespace__Field`.

### placeholder [String]

Text to show as placeholder on inputs. Doesn't apply to dates/datetimes

### disabled [Boolean]
Whether the input is disabled or not
 
### notInclude[Array]
For picklists fields, allow to hide the values.

### format [String]
> Valid values are `'iso', 'locale', 'timestamp'`

> Default `'timestamp'`

For dates and datetimes, this props set on which format will be set on the model.



## Methods
These methods are accesible using `v-ref` on component.

### getRecord()
Useful for lookup fields. Returns a copy of the auxiliar selected record in the lookup. The fields of the record will be the fields displayed in the lookup modal.

## Events
### input
When the value changes.

## Salesforce config
* The input wont display if the current user doen´t not have permissions to see the field.
