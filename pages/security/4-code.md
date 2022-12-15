<StandardTab choosen="security" />

<div class="my-4"></div>

<div class="flex items-end space-x-5">
  <h6>Code Implementation</h6>
  <span class="text-sm text-gray-400">Create endpoint registration</span>
</div>

<div class="h-96 overflow-y-auto my-4">
```ts {21-31|33-40} 
interface User {
  id: number // auto generate number
  firstName?: string
  lastName?: string
  email: string
  password: string
}

export const create = async (req: Request, res: Response, next: NextFunction) => {
  try {
    // 1. get data from client
    const data:User = req.body

    // 2. validate data from client
    if (!data.email) {
      return res.status(422).json('email is required')
    } else if (!data.password) {
      return res.status(422).json('password is required')
    }

    if (data.password) {
      if (data.password.length < 8) {
        return res.status(422).json('password should have greater than or equal to 8 digit')
      } else {
        if (data.password.match(/^[0-9a-z]+$/)) {
          return res.status(422).json('password should contains alphanumeric')
        } else if (data.password.match(/[`!@#$%^&*()_+\-=\[\]{};':"\\|,.<>\/?~]/)) {
          return res.status(422).json('password should have symbol')
        }
      }
    }

    const isExists = await db.collection('users').find({ email: data.email })

    // 3. insert data to database
    if (!isExists) {
      const result = await db.collection('users').create(data)
    } else {
      return res.status(422).json('email already exists in database')
    }
    
    // 4. send response from client
    res.status(201).json({
      id: result.id,
    });
  } catch (error) {
    next(error);
  }
};

```
</div>
<!-- TIME : 05:00 -->