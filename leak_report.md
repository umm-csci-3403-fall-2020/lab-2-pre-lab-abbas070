# Leak report

Function free() has to be added in the code, which will only run once, so that the memory can be cleaned. Without this function you will have memory leaks. Otherwise, the function would not be valib

int is_clean(char* str) {
char* cleaned;
int result;

cleaned = strip(str);

result = strcmp(str, cleaned);

return result == 0;

}

This method would be running once so that the free() function would have to be implemented in this method.
