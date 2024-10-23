
```tasks
filter by function ! task.isDone
# group by function task.file.root

group by function \
    const date = task.due.moment; \
    const tomorrow  = moment().add(1,'days'); \
    const nextthreedays = moment().add(4,'days'); \
    const inaweek = moment().add(7,'days'); \
    const now = moment(); \
    const label = (order, name) => `%%${order}%% ==${name}==`; \
    if (!date)                           return label(7, 'Undated'); \
    if (!date.isValid())                 return label(0, 'Invalid date'); \
    if (date.isBefore(now, 'day'))       return label(1, 'Overdue'); \
    if (date.isSame(now, 'day'))         return label(2, 'Today'); \
    if (date.isSame(tomorrow, 'day'))    return label(3, 'Tomorrow'); \
    if (date.isBefore(nextthreedays, 'day')) return label (4, 'Within a few days'); \
    if (date.isBefore(inaweek, 'day'))   return label(5, 'Within a week'); \
    return label(6, 'Future');

group by function task.file.root
short mode
```
