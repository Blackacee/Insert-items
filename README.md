# Insert-items

/* Syntax:
 array.insert(index, value1, value2, ..., valueN) */
Array.prototype.insert = function(index) {
 this.splice.apply(this, [index, 0].concat(
 Array.prototype.slice.call(arguments, 1)));
 return this;
};
["a", "b", "c", "d"].insert(2, "X", "Y", "Z").slice(1, 6); // ["b", "X", "Y", "Z", "c"]
